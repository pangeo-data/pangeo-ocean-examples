# Note that there must be a tag
FROM pangeo/pangeo-notebook:2019.05.23

# this should get upstreamed
RUN pip install eofs

# https://mybinder.readthedocs.io/en/latest/tutorials/dockerfile.html#preparing-your-dockerfile
ENV NB_USER jovyan
ENV NB_UID 1000
ENV HOME /home/${NB_USER}

COPY . ${HOME}
USER root
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}
