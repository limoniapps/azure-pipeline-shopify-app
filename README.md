# azure-pipeline-shopify-app
This repository simply contains a sample Azure DevOps pipeline that can be used to deploy a Shopify App.

It assumes that you:
- define a variable (secret preferably) named cliPartnerToken on your Azure DevOps pipeline (https://learn.microsoft.com/en-us/azure/devops/pipelines/process/set-secret-variables)
- use Rust to code your functions

Further, the pipeline assumes a folder structure similar to this:
|--azure-pipelines.yml
|-- src
    |
    |-- package.json
    |-- .env
    |-- shopify.app.toml
    |-- extensions
        |
        |-- function1
            |-- src
                |
                |-- function1.rs
                |-- ...
            |-- cargo.toml
            |-- shopify.function.extension.toml
        |-- function2
        |-- ...
        |-- extensions
        |-- ...
