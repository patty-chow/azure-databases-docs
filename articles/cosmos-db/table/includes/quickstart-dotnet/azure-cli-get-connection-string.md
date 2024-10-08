---
ms.service: azure-cosmos-db
ms.subservice: table
ms.topic: include
ms.date: 08/23/2024
---
1. Find the API for Table **connection string** from the list of connection strings for the account with the [``az cosmosdb list-connection-strings``](/cli/azure/cosmosdb#az-cosmosdb-list-connection-strings) command.

    ```azurecli-interactive
    az cosmosdb list-connection-strings \
        --resource-group $resourceGroupName \
        --name $accountName 
    ```

1. Record the *Primary Table Connection String* values. You'll use these credentials later.
