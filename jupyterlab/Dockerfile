FROM jupyter/minimal-notebook

USER root



USER $NB_UID

# Conda packages
RUN conda install --quiet --yes \
    jupyterhub \
    conda clean -tipsy && \
    fix-permissions $CONDA_DIR

ENV CPATH=$CONDA_DIR/include

USER $NB_UID

# Add conda env hook
COPY ./conda-activate.sh /usr/local/bin/before-notebook.d/
