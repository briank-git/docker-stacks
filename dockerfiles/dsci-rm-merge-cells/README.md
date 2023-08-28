When using the `dsci-rm-merge-cells` Docker image with JupyterHub and DockerSpawner, 
be sure to set `c.DockerSpawner.post_start_cmd = 'sh -c "cp -a /tmp/user-settings/. /home/jupyter/.jupyter/lab/user-settings"'` 
in `/srv/jupyterhub/jupyterhub_config.py`.

Required packages are listed under dependencies in the environment.yml file. If any changes are made to environment.yml, make sure to run `conda-lock --mamba -k explicit --file environment.yml -p linux-64` in the same directory to create a fresh lock file before building the Docker image.