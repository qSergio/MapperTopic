ARG BASE_CONTAINER=jupyter/minimal-notebook
FROM $BASE_CONTAINER
LABEL author="Sam NM"
USER root
RUN mkdir /home/jovyan/code
WORKDIR /home/jovyan/code
ADD requirements.txt /home/jovyan/code/
RUN \
    #apt-get update && \
    pip install --upgrade pip && \
    pip install -r requirements.txt --no-cache-dir
# RUN pip install pandas numpy matplotlib plotly
# Switch back to jovyan to avoid accidental container runs as root
WORKDIR /home/jovyan
USER $NB_UID