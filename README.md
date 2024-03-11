# Purpose
This repository provides a sample Azure DevOps pipeline (azure-pipelines.yml) that can be used as a starting point to deploy a Shopify App.

# Assumptions
- The pipeline assumes you've selected Rust to code your functions (if any).
- The pipeline assumes you have a package-lock.json file. It uses the hash of this file as part of the cache key. If you've selected to .gitignore this file, use package.json instead.

# Steps
- Add the azure-pipelines.yml file included in this repository to yours
- Add a secret variable named cliPartnerToken to your Azure DevOps pipeline (https://learn.microsoft.com/en-us/azure/devops/pipelines/process/set-secret-variables)

# Folder structure
The pipeline assumes a folder structure similar to this:
```bash
├── azure-pipelines.yml
└── src
    ├── package.json
    ├── package-lock.json
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

