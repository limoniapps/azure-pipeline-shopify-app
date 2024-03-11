# Purpose
This repository provides a sample Azure DevOps pipeline (azure-pipelines.yml) that can be used as a starting point to deploy a Shopify App.

# Assumptions
The pipeline assumes you've selected Rust to code your functions (if any).

# Steps
- Add the azure-pipelines.yml file included in this repository to yours
- Add a secret variable named cliPartnerToken to your Azure DevOps pipeline (https://learn.microsoft.com/en-us/azure/devops/pipelines/process/set-secret-variables)

# Folder structure
The pipeline assumes a folder structure similar to this:
```bash
├── azure-pipelines.yml
└── src
    ├── package.json
    ├── .env
    ├── shopify.app.toml
    └── extensions
        ├── sample-function
        |   ├── src
        |   |   ├── .rs
        |   |   └── ...
        |   ├── cargo.toml
        |   └── shopify.function.extension.toml
        ├── extensions
        |   ├── assets
        |   ├── blocks
        |   ├── locales
        |   ├── snippets
        |   └── shopify.function.extension.toml
        └── ...
```

