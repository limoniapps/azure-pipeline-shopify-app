# Purpose
This repository provides a sample Azure DevOps pipeline (azure-pipelines.yml) that can be used as a starting point to deploy a Shopify App.

# Assumptions
- The pipeline assumes you're using npm as the package manager.
- The pipeline assumes you've selected Rust to code your functions (if any).
- The pipeline assumes you have a `package-lock.json` file.
  It uses the hash of this file as part of the cache key.
  If you've selected to `.gitignore` this file, change the variable `npmModulesCacheKey` to `package.json` instead.

# Steps
- Add the `azure-pipelines.yml` file included in this repository to yours.
- Add a secret variable named `cliPartnerToken` to your Azure DevOps pipeline as documented [here](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/set-secret-variables).
- Edit the `azure-pipelines.yml` file to set a value for the variables `appClientId` and `functionFolders`
- Verify that your files are structured as explained in the folder structure below.
  If not, make the necessary adjustments in the `azure-pipelines.yml` file.

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

