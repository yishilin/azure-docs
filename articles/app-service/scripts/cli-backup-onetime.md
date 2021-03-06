---
title: 'CLI: Back up an app'
description: Learn how to use the Azure CLI to automate deployment and management of your App Service app. This sample shows how to back up an app.
author: msangapu-msft
tags: azure-service-management

ms.devlang: azurecli
ms.topic: sample
ms.date: 12/07/2017
ms.author: msangapu
ms.reviewer: cephalin
ms.custom: mvc, seodec18, devx-track-azurecli
---

# Back up an app using CLI

This sample script creates an app in App Service with its related resources, and then creates a one-time backup for it. 

[!INCLUDE [quickstarts-free-trial-note](../../../includes/quickstarts-free-trial-note.md)]

[!INCLUDE [cloud-shell-try-it.md](../../../includes/cloud-shell-try-it.md)]

If you choose to install and use the CLI locally, you need Azure CLI version 2.0 or later. To find the version, run `az --version`. If you need to install or upgrade, see [Install the Azure CLI]( /cli/azure/install-azure-cli).

## Sample script

[!code-azurecli-interactive[main](../../../cli_scripts/app-service/backup-onetime/backup-onetime.sh?highlight=3-7 "Back up an app")]

[!INCLUDE [cli-script-clean-up](../../../includes/cli-script-clean-up.md)]

## Script explanation

This script uses the following commands. Each command in the table links to command specific documentation.

| Command | Notes |
|---|---|
| [`az group create`](/cli/azure/group#az-group-create) | Creates a resource group in which all resources are stored. |
| [`az storage account create`](/cli/azure/storage/account#az-storage-account-create) | Creates a storage account. |
| [`az storage container create`](/cli/azure/storage/container#az-storage-container-create) | Creates an Azure storage container. |
| [`az storage container generate-sas`](/cli/azure/storage/container#az-storage-container-generate-sas) | Generates an SAS token for an Azure storage container.  |
| [`az appservice plan create`](/cli/azure/appservice/plan#az-appservice-plan-create) | Creates an App Service plan. |
| [`az webapp create`](/cli/azure/webapp#az-webapp-create) | Creates an App Service app. |
| [`az webapp config backup create`](/cli/azure/webapp/config/backup#az-webapp-config-backup-create) | Creates a backup for an App Service app. |
| [`az webapp config backup list`](/cli/azure/webapp/config/backup#az-webapp-config-backup-list) | Gets a list of backups for an App Service app. |

## Next steps

For more information on the Azure CLI, see [Azure CLI documentation](/cli/azure).

Additional App Service CLI script samples can be found in the [Azure App Service documentation](../samples-cli.md).
