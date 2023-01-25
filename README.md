# deploy-azure-app-service

This repository deploys a .NET WebAPI to Azure via GitHub Actions.

Additionally:
* An Azure Service Principal is used
* An Azure ARM Bicep template is used to create the app service

## GitHub Repository Settings

* Create an `AZURE_CREDENTIALS` secret in the repo and set it to the value of your Azure Security Principal
* Optionally, set a **wait timer** environment protection rule for the `Clean` environment. This will cleanup the resource group after the time passes.

## Verify the App Service is Working

Once the deployment is successful, go to https://{hostname}/WeatherForecast to verify.
