### Documentation Referred:

https://registry.terraform.io/

https://registry.terraform.io/providers/hashicorp/aws/latest/docs

### first_ec2.tf

```sh
provider "aws" {
  region     = "us-east-1" # Your region
  access_key = "PUT-YOUR-ACCESS-KEY-HERE"
  secret_key = "PUT-YOUR-SECRET-KEY-HERE"
}

# Can declare more than one provider

resource "aws_instance" "myec2" {
    ami = "ami-00c39f71452c08778" # Changed with respect to region as well
    instance_type = "t2.micro"
}
```

### Commands:

```sh
terraform init
terraform plan
terraform apply
```
