# setup-terraform

This GitHub Action is a wrapper for [`hashicorp/setup-terraform`](https://github.com/hashicorp/setup-terraform), it exposes the action inputs except for `cli_config_credentials_token` since Terraform Cloud will not be used. It authenticates automatically with a preconfigured custom HTTP state backend.


### Usage
```yml
steps:
- uses: narwhl/setup-terraform@v1
  with:
    terraform_version: "1.7.1"

```

### Action Inputs

- `terraform_version`

- `terraform_wrapper`

- `state` path to store the terraform state, must be unique per workflow

- `use_federated_token` uses token issued by [sts](https://github.com/narwhl/imprint), it has the validity of 1 hr instead of 5mins from github

- `endpoint` preconfigured