# io-infrastructure-pipelines

This repository collects a set of pipelines aming to automate some common and ripetitive tasks useful to maintein the cloud infrastructure hosting the backend of the [mobile app IO](https://io.italia.it/).

The pipelines are designed to run within Azure DevOps.

Also refer to these repositories to have an overview of the cloud infrastrucure:

* [Terraform modules](https://github.com/pagopa/io-infrastructure-modules-new)
* [Terragrunt infrastructure](https://github.com/pagopa/io-infrastructure-live-new)

## Backup key vault secrets

* [backup-secrets-pipeline.yaml](./pipelines/backup-secrets-pipeline.yaml)

It copies all secrets stored in a key vault to a storage account.
Screts are encrypted with the key vault key.

## Backup Api Management.

* [backup-apim-pipeline](./pipelines/backup-apim-pipeline.yaml)

This pipeline is useful to backup users, subscriptions and groups of an instance of [Azure Api Management](https://docs.microsoft.com/en-us/rest/api/apimanagement/).
 The backup is stored in a storage account and can be restored with the appropriate PowerShell command shown in the [official documentation](https://docs.microsoft.com/en-us/azure/api-management/scripts/powershell-backup-restore-apim-service).

### Reference

* [Api Management backup and restore](https://docs.microsoft.com/en-us/azure/api-management/scripts/powershell-backup-restore-apim-service)
