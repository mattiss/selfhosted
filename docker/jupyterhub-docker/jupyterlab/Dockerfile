FROM atoti/atoti:latest

USER root

# APT packages
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git

USER $NB_UID

# Conda packages
RUN conda install -c conda-forge jupyterlab jupyterlab-git nbdime && \
    jupyter server extension enable --py jupyterlab_git && \
    jupyter lab build

ENV JUPYTER_ENABLE_LAB=true
