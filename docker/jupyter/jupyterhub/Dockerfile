FROM jupyterhub/jupyterhub:1.4.0

RUN pip install \
    dockerspawner==12.0.0 \
    oauthenticator==14.0.0 \
    jupyterhub-idle-culler==1.1

COPY jupyterhub_config.py .
COPY templates/* ./templates/

