# Url Shortner

## Infrastructure as Code 

### Log in into Azure
```bash
az login
```

### Create Resource Group
```bash
az group create --name urlshortner-dev --location westeurope
```

### Create User for GH Actions
```bash
az ad sp create-for-rbac \
    --name "GitHub-Actions-SP" \
    --role contributor \
    --scopes /subscriptions/dd627ee9-2a7b-4650-9ab6-6b4436401b7f \
    --sdk-auth                        
```

### Configure a federated identity credential on an app

