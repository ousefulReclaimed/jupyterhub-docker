FROM jupyterhub/jupyterhub
COPY jupyterhub_config.py .

RUN apt-get update && \
    apt-get install -y --no-install-recommends wget && \
    apt-get clean && rm -rf /var/lib/apt/lists/*
RUN wget https://raw.githubusercontent.com/jupyterhub/jupyterhub/0.9.3/examples/cull-idle/cull_idle_servers.py

RUN pip install \
    dockerspawner==0.10.0 \
    jupyterhub-firstuseauthenticator
