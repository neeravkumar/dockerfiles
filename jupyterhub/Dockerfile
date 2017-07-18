FROM jupyterhub/jupyterhub:latest
RUN pip install notebook && apt-get update && apt-get install python python-dev build-essential -y &&\
    wget https://bootstrap.pypa.io/get-pip.py && python2 get-pip.py && rm get-pip.py &&\
    python2 -m pip install ipykernel && python2 -m ipykernel install && apt-get clean all &&\
    conda install nodejs -y && npm install -g ijavascript && ijsinstall --install=global &&\
    jupyter notebook --generate-config --allow-root && mkdir /etc/jupyter &&\
    mv /root/.jupyter/jupyter_notebook_config.py /etc/jupyter &&\
    echo "c.NotebookApp.allow_origin = '*'" >> /etc/jupyter/jupyter_notebook_config.py
