FROM jupyter/scipy-notebook:latest

USER root


RUN apt-get update --yes && \
    apt-get install --yes \
    --no-install-recommends \
    curl 
#    && \
RUN    apt-get clean && rm -rf /var/lib/apt/lists/*

USER ${NB_UID}

# install necessary python modules
RUN pip3 install openpyxl pymysql tabulate mysql-connector-python

RUN fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
