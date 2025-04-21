## Install and Cache Terraform Plugin

![Commit Activity](https://img.shields.io/github/commit-activity/t/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![Last Commit](https://img.shields.io/github/last-commit/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![Release Date](https://img.shields.io/github/release-date/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![Repo Size](https://img.shields.io/github/repo-size/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![File Count](https://img.shields.io/github/directory-file-count/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![Issues](https://img.shields.io/github/issues/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![Top Language](https://img.shields.io/github/languages/top/subhamay-bhattacharyya-gha/terraform-plugin-action)&nbsp;![Custom Endpoint](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/bsubhamay/e37596a21f01bae51fb3b05e540329af/raw/terraform-plugin-action.json?)

This GitHub Action sets up Terraform and optionally caches its plugin directory to speed up workflow execution.

## Features

- Installs a specific version of Terraform.
- Optionally caches the Terraform plugin directory (`~/.terraform.d/plugin-cache`).
- Outputs whether the cache was used.

## Inputs

| Name        | Description                                | Required | Default |
|-------------|--------------------------------------------|----------|---------|
| `caching`   | Whether to cache dependencies or not.      | No       | `true`  |
| `tf-version`| The Terraform version to be used.          | Yes      | `1.4`   |

## Outputs

| Name         | Description                          |
|--------------|--------------------------------------|
| `used-cache` | Whether the cache was used.          |

## Example Usage

```yaml
jobs:
  terraform:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Install and Cache Terraform Plugin
        uses: subhamay-bhattacharyya-gha/terraform-plugin-action@main
        with:
          tf-version: 1.4
          caching: true
```

## License

MIT
