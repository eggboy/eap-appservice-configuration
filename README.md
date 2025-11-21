[![Deploy module changes to App Service](https://github.com/eggboy/eap-appservice-configuration/actions/workflows/blank.yml/badge.svg)](https://github.com/eggboy/eap-appservice-configuration/actions/workflows/blank.yml)

# Migrate and Modernize JBoss EAP on Azure App Service (PaaS)
Check the full article here: https://eggboy.medium.com/migrate-and-modernize-jboss-eap-on-azure-app-service-paas-fe0e0ec3fcb6

# eap-appservice-configuration

Steps to deploy to App Service

1. Using an FTP client of your choice, upload your JDBC driver, jboss-cli-commands.cli, startup_script.sh, to /site/deployments/tools/. FTP credentials can be found under **Deployment Center > FTPS credentials**
2. Configure your site to run startup_script.sh when the container starts. In the Azure portal, navigate to **Configuration > General Settings > Startup Command**. Set the startup command field to /home/site/deployments/tools/startup_script.sh, then select Save.

```
# curl -vvv https://jboss-eap.azurewebsites.net/jay/
*****
< Transfer-Encoding: chunked
< Content-Type: application/json
< Vary: Access-Control-Request-Headers
< Server: N/A
< X-Powered-By: Undertow/1
< X-XSS-Protection: X-XSS-Protection=1; mode=block
< X-Frame-Options: sameorigin
< Content-Security-Policy: text/html
< X-Content-Type-Options: X-content-type-options:nosniff
< Strict-Transport-Security: max-age=3153600
```

# Enabling Access logs for JBoss 7
https://access.redhat.com/solutions/2423311
