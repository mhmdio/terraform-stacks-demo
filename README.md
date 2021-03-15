# Terraform Stacks Demo

Mono Repo Terraform Layout. Based on Vanilla Terraform, this layout used in CI/CD tools, another demo will be provided for Terraform Cloud.

- bootstrap: contains Terraform bootstrap for S3 bucket, KMS key and Dynamodb table for State files.
- config: config files for all 3rd party tools that used with Terraform.
- docs: Documentation related file.
- envs: contains environments tfvars values for  state file and stack
- modules: Terraform modules root folder
- stacks: Terraform templates that define a working unit.

## Layout

```bash
├── README.md
├── bootstrap
│   ├── README.md
│   ├── dev
│   │   └── bootstrap.tf
│   ├── prod
│   │   └── bootstrap.tf
│   └── stage
│       └── bootstrap.tf
├── config
│   ├── README.md
│   ├── atlantis.yml
│   ├── infracost.yml
│   ├── terraform-docs.yml
│   └── tfsec.yml
├── docs
│   └── README.md
├── envs
│   ├── README.md
│   ├── dev
│   │   └── us-east-1
│   │       ├── README.md
│   │       ├── bakend.tfvars
│   │       └── dev.tfvars
│   ├── mgmt
│   │   └── us-east-1
│   │       ├── README.md
│   │       ├── bakend.tfvars
│   │       └── mgmt.tfvars
│   ├── prod
│   │   ├── us-east-1
│   │   │   ├── README.md
│   │   │   ├── bakend.tfvars
│   │   │   └── prod.tfvars
│   │   └── us-west-1
│   │       ├── README.md
│   │       ├── bakend.tfvars
│   │       └── prod.tfvars
│   └── stage
│       └── us-east-1
│           ├── README.md
│           ├── bakend.tfvars
│           └── stage.tfvars
├── modules
│   └── README.md
└── stacks
    ├── README.md
    ├── app
    │   ├── README.md
    │   ├── main.tf
    │   ├── outputs.tf
    │   └── variables.tf
    ├── data
    │   ├── README.md
    │   ├── main.tf
    │   ├── outputs.tf
    │   └── variables.tf
    ├── mgmt
    │   ├── README.md
    │   ├── main.tf
    │   ├── outputs.tf
    │   └── variables.tf
    └── network
        ├── README.md
        ├── main.tf
        ├── outputs.tf
        └── variables.tf
```