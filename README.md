# Azure Container Apps - Infrastructure Template 

## Manual Deployment
```
az deployment sub create --location northeurope --template-file infrastructure/main.bicep --parameters infrastructure/params.json
```


## Github Action Deployment

When generating your credentials (in this example we store in a secret named AZURE_CREDENTIALS) you will need to specify a scope at the subscription level.

```
az ad sp create-for-rbac --name "{sp-name}" --sdk-auth --role contributor --scopes /subscriptions/{subscription-id}
```