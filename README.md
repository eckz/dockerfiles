# dockerfiles

## eckz/octave-notebook

Jupyter notebook that depends on jupyter/scipy-notebook and includes the octave kernel

    docker run -d -p 8888:8888 --name jupyter-octave -v $HOME/notebooks:/home/jovyan/work eckz/octave-notebook
    docker logs jupyter-octave

## eckz/mxnet-notebook

Jupyter notebook that depends on jupyter/tensorflow-notebook and includes mxnet version 0.12

    docker run -d -p 8888:8888 --name jupyter-mxnet -v $HOME/notebooks:/home/jovyan/work eckz/mxnet-notebook
    docker logs jupyter-mxnet

Ports:
 - 8888: Http interface to access the notebook

## eckz/mailcatcher

Mailcatcher daemon

    docker run -d -P --name mailcatcher eckz/mailcatcher

Ports:
 - 1025: SMTP server, you should send your emails here
 - 1080: Http interface to read the emails