# setup-terraform

This GitHub Action is a wrapper for `[hashicorp/setup-terraform](https://github.com/hashicorp/setup-terraform)`, it exposes the same action inputs except for `cli_config_credentials_token` since Terraform Cloud will not be used. It also add extra steps to configure settings to ensure compatibility with custom S3 backend (e.g Cloudflare R2 / Minio)

```yml
steps:
- uses: narwhl/setup-terraform@v1
  with:
    terraform_version: "1.7.1"

```
