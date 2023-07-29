## variables.tf

This file contains variables for the configuration. It's in a separate file to make it easier to organize/understand, although it could be included in the `main.tf` file.

```terraform
variable "project" { }

variable "credentials_file" { }

variable "region" {
  default = "us-central1"
}

variable "zone" {
  default = "us-central1-c"
}
```

- If a default value is set, the variable is optional
- Variable definitions with a blank block `{ }` will be required, and will prompt for values when running `terraform plan`.

This file can be checked into source control, but don't include any sensitive info.

## terraform.tfvars

Variables can be populated using values from this file. **Do not check this file into source control.**

```terraform
project                  = "potent-density-394317"
credentials_file         = "potent-density-394317-9a30b5909c20.json"
```
