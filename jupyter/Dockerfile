FROM python



RUN useradd liszt && mkdir /home/liszt && chown liszt:liszt /home/liszt && mkdir /home/liszt/notebook && chown liszt:liszt /home/liszt/notebook && \ 
    pip install jupyterlab -i https://pypi.tuna.tsinghua.edu.cn/simple
USER liszt
COPY ./jupyter_lab_config.py /home/liszt/.jupyter/jupyter_lab_config.py
WORKDIR /home/liszt/notebook
VOLUME /home/liszt/notebook
EXPOSE 15751

CMD [ "jupyter", "lab" ]
