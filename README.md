# Terraform Infrastructure as Code (IaC) - Azure Labels Module

## Table of Contents
- [Introduction](#introduction)
- [Usage](#usage)
- [Module Inputs](#module-inputs)
- [Module Outputs](#module-outputs)
- [Authors](#authors)
- [License](#license)

## Introduction
This Terraform module creates structured labels for Azure resources with specific attributes.

## Usage

- Use the module by referencing its source and providing the required variables.

```hcl
    module "labels" {
      source        = "git::https://github.com/yadavprakash/terraform-azure-labels.git?ref=v1.0.0"  # Update with the correct path to the module
      name          = "app"
      environment   = "test"
      label_order   = ["name", "environment"]
      business_unit = "Corp"
      attributes    = ["private"]
      extra_tags = {
        Application = "Demo"
      }
    }
```
Please ensure you specify the correct 'source' path for the module.

## Module Inputs

- `name`: The name of the application or resource.
- `environment`: The environment in which the resource exists.
- `label_order`: The order in which labels should be applied.
- `business_unit`: The business unit associated with the application.
- `attributes`: Additional attributes to add to the labels.
- `extra_tags`: Extra tags to associate with the resource.

## Module Outputs
- This module currently does not provide any outputs.

# Examples
For detailed examples on how to use this module, please refer to the '[example](https://github.com/yadavprakash/terraform-azure-labels/tree/master/_example)' directory within this repository.

## Authors
Your Name
Replace '[License Name]' and '[Your Name]' with the appropriate license and your information. Feel free to expand this README with additional details or usage instructions as needed for your specific use case.

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/yadavprakash/terraform-azure-labels/blob/master/LICENSE) file for details.


