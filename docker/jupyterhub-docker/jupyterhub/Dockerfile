FROM jupyterhub/jupyterhub:1.4.2

RUN pip install \
    dockerspawner==12.1.0 \
    oauthenticator==14.2.0 \
    jupyterhub-idle-culler==1.2

COPY jupyterhub_config.py .
COPY templates/* ./templates/

