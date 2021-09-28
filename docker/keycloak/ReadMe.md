# Initialization
Create the admin user by running the following commands
```bash
docker exec keycloak /opt/jboss/keycloak/bin/add-user-keycloak.sh -u <${ADMIN_USER}> -p <${ADMIN_PASSWORD}>
docker restart keycloak
```
Then go to 

https://auth.${MY_DOMAIN}/auth/admin