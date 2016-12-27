# dockerfiles

## eckz/octave-notebook

Jupyter notebook that depends on jupyter/scipy-notebook and includes the octave kernel

    docker run -d -P --name octave -v $(pwd):/home/jovyan/work eckz/octave-notebook
    docker port octave

Ports:
 - 8888: Http interface to access the notebook

## eckz/mailcatcher

Mailcatcher daemon

    docker run -d -P --name mailcatcher eckz/mailcatcher

Ports:
 - 1025: SMTP server, you should send your emails here
 - 1080: Http interface to read the emails