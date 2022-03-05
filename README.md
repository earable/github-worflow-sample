# github-worflow-sample

Dev needs to correct the following values in workflow files:

APP_NAME: is the << service name >> identifier when deploying to K8s (Devops set this env), refer to the service identifier for each environment at https://earable.atlassian.net/wiki/spaces/EARABLE/pages/148144129

HEALTHCHECK_URL: A << service endpoint >> that Dev calls to perform a system health check after deploying (path to system api /health, refer to the identifiers of api endpoints for each environment at https://earable.atlassian.net/wiki/spaces/EARABLE/pages/148144129), or trigger to a service test to do post-testing after deploy.
