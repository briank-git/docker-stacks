# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
# TODO: For testing purposes only, replace with ubcmds/dsci-011:latest
FROM brianki/kcds-student-test:29-08-2023

LABEL maintainer="Brian Kim <brian.kim@stat.ubc.ca>"

# Install nbgrader via mamba
RUN mamba install --quiet --yes \
    'nbgrader' && \
    mamba clean --all -f -y

# re-upgrade jupyter-server (mamba downgrades it)
RUN pip install --upgrade jupyter-server

