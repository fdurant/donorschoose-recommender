FROM continuumio/anaconda3
MAINTAINER Frederik Durant <frederik.durant@pandora.be>

RUN /opt/conda/bin/conda install jupyter -y --quiet && \
    mkdir /notebooks && \
    mkdir /data

VOLUME ["/data","/notebooks"]

EXPOSE 8888

CMD jupyter notebook --notebook-dir=notebooks --ip='*' --port=8888 --no-browser --allow-root --NotebookApp.token='donorschoose'
