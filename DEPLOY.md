# Dev Deployment

## Authenicate to Azure CLI
az login

## Set Target Azure Subscription
az account set --subscription "cie-dev"

## Engine Container
az acr build -r ciedevsharedacr -t ipam-engine:latest -f ./engine/Dockerfile.rhel ./engine

## UI Container
az acr build -r ciedevsharedacr -t ipam-ui:latest -f ./ui/Dockerfile.rhel ./ui