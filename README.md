# io-infrastructure-pipelines

This repository collects a set of pipelines aming to automate some common and ripetitive task useful to maintein the cloud infrastructure hosting the backend of the [mobile app IO](https://io.italia.it/).

The pipelines are designed to run within Azure DevOps.

Also refer to these repositories to have an overview of the cloud infrastrucure:

* [Terraform modules](https://github.com/pagopa/io-infrastructure-modules-new)
* [Terragrunt infrastructure](https://github.com/pagopa/io-infrastructure-live-new)

## Backup key vault secrets

* [backup-secrets-pipeline.yaml](./pipelines/backup-secrets-pipeline.yaml)

It  copies all secrets stored in a key vault to a storage account.
Screts are encrypted with the key vault key.
