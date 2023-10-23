# Infrastructure as Code with Terraform on Azure

This repository contains the Terraform configuration to deploy a simple Azure infrastructure using the [Quickstart: Use Terraform to create a Linux VM](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-terraform?tabs=azure-cli) guide.

## Infrastructure Overview

This Terraform script deploys the following components in Azure:

- Azure Resource Group: A container for Azure resources.
- Virtual Network: A virtual network to which the VM will be connected.
- Linux Virtual Machine: A Linux-based virtual machine with basic configurations.
- Network Security Group (NSG): A basic NSG with some rules to control network traffic.

## Diagram

Here is an architectural diagram illustrating the deployed infrastructure:

![Infrastructure Diagram](diagram.png)

## How to Deploy

To deploy this infrastructure, follow these steps:

1. Clone this repository to your local machine.
2. Make sure you have [Terraform](https://www.terraform.io/downloads.html) installed.
3. Configure your Azure credentials using `az login`.
4. Initialize the Terraform working directory: `terraform init`.
5. Review and customize the `main.tf` file to match your preferences.
6. Apply the configuration to create the Azure resources: `terraform apply`.
7. Verify the deployment in your Azure portal.

## Contributors

This project welcomes contributions and suggestions. If you would like to contribute to the Terraform configuration, please follow the [Module Contribution Guide](./module/CONTRIBUTE.md) and [Provider Contribution Guide](./provider/CONTRIBUTE.md).

## Code of Conduct

This project follows the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

Feel free to reach out if you have any questions or need further assistance with this project.

