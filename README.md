[![Doodba deployment](https://img.shields.io/badge/deployment-doodba-informational)](https://github.com/Tecnativa/doodba)
[![Last template update](https://img.shields.io/badge/last%20template%20update-v8.3.10-informational)](https://github.com/Tecnativa/doodba-copier-template/tree/v8.3.10)
[![Odoo](https://img.shields.io/badge/odoo-v18.0-a3478a)](https://github.com/odoo/odoo/tree/18.0)
[![BSL-1.0 license](https://img.shields.io/badge/license-BSL--1.0-success})](LICENSE)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://pre-commit.com/)

# doodba-template - a Doodba deployment

This project is a Doodba scaffolding. Check upstream docs on the matter:

- [General Doodba docs](https://github.com/Tecnativa/doodba).
- [Doodba copier template docs](https://github.com/Tecnativa/doodba-copier-template)
- [Doodba QA docs](https://github.com/Tecnativa/doodba-qa)

## Using `git-aggregate` with Selective Module Checkout

This project extends the standard `git-aggregate` command to support **downloading only
selected modules** from a repository, based on your `addons.yaml` configuration.

## Command

To aggregate repositories and apply Sparse Checkout rules:

```python
inv git-aggregate --clean
```

The `--clean` flag runs a cleanup process that applies the Sparse Checkout settings
according to your addons.yaml.

## Benefits

- Reduced storage usage.
- Faster git-aggregate execution, especially on large OCA/community repositories.
- No manual repo cleanup required when changing module selection.

# Credits

This project is maintained by: Ecosoft
