# tf-aws-infra

## Assignment 3

### Step 1:
Make sure you have an AWS account, AWS Access key and Secret Access Key.
You can create an AWS account and get your access key and secret key from the AWS IAM dashboard.

### Step 2
Clone repository and navigate to the folder in Termainl or your preferred Command Line.

### Step 3
Create a file named `terraform.tfvars` in the root of the project with the following content:
```
region = "us-east-1"
vpc_cidr = "10.0.0.0/16" # CIDR block for the VPC
public_subnet_cidrs = [ "10.0.0.0/20", "10.0.16.0/20", "10.0.32.0/20"] # CIDR blocks for the public subnets
private_subnet_cidrs = [ "10.0.128.0/20", "10.0.144.0/20", "10.0.160.0/20"] # CIDR blocks for the private subnets
availability_zones = ["us-east-1a", "us-east-1b", "us-east-1c"]
```

### Step 4
Configure your AWS Profile using the command ' aws configure --profile=<profile_name>'
Enter the following when prompted:
```
AWS Access Key ID [None]: <access_key>
AWS Secret Access Key [None]: <secret_access_key>
Default region name [None]: us-east-1
Default output format [None]: json
```

To use the profile, use command ' export AWS_PROFILE=<profile_name>'

### Step 5
Run the following command to initialize Terraform:
```
terraform init
terraform plan
terraform apply
```

## Assignmetnt 4

`terraform.tfvars` 
```
region               = "us-east-1"
vpc_cidr             = "10.0.0.0/16"                                       # CIDR block for the VPC
public_subnet_cidrs  = ["10.0.0.0/20", "10.0.16.0/20", "10.0.32.0/20"]     # CIDR blocks for the public subnets
private_subnet_cidrs = ["10.0.128.0/20", "10.0.144.0/20", "10.0.160.0/20"] # CIDR blocks for the private subnets
availability_zones   = ["us-east-1a", "us-east-1b", "us-east-1c"]
instance_type        = "t2.micro"
custom_ami_id        = "ami-0a61753b57d61737d" # Get AMI from AWS Console
key_pair_name        = "keypair"
```

## Assignmetnt 5

`terraform.tfvars` 
```
region               = "us-east-1"
vpc_cidr             = "10.0.0.0/16"                                       # CIDR block for the VPC
public_subnet_cidrs  = ["10.0.0.0/20", "10.0.16.0/20", "10.0.32.0/20"]     # CIDR blocks for the public subnets
private_subnet_cidrs = ["10.0.128.0/20", "10.0.144.0/20", "10.0.160.0/20"] # CIDR blocks for the private subnets
availability_zones   = ["us-east-1a", "us-east-1b", "us-east-1c"]
instance_type        = "t2.micro"
custom_ami_id        = "ami-0a61753b57d61737d" # Get AMI from AWS Console
key_pair_name        = "keypair"
application_port     = 8080
database_port        = 5432
db_username          = "csye6225"
db_password          = "csye6225"
```

## Assignmetnt 6

`terraform.tfvars` 
```
region               = "us-east-1"
vpc_cidr             = "10.0.0.0/16"                                       # CIDR block for the VPC
public_subnet_cidrs  = ["10.0.0.0/20", "10.0.16.0/20", "10.0.32.0/20"]     # CIDR blocks for the public subnets
private_subnet_cidrs = ["10.0.128.0/20", "10.0.144.0/20", "10.0.160.0/20"] # CIDR blocks for the private subnets
availability_zones   = ["us-east-1a", "us-east-1b", "us-east-1c"]
instance_type        = "t2.micro"
custom_ami_id        = "ami-0ca2b2f5618ba7cc7"
key_pair_name        = "keypair"
application_port     = 8080
database_port        = 5432
db_username          = "csye6225"
db_password          = "csye6225"
zone_id              = "<zone_id>"
subdomain_name       = "<subdomain_name>"
aws_account_id       = <aws_account_id>
```

## Assignmetnt 8

`terraform.tfvars` 
```
region               = "us-east-1"
vpc_cidr             = "10.0.0.0/16"                                       # CIDR block for the VPC
public_subnet_cidrs  = ["10.0.0.0/20", "10.0.16.0/20", "10.0.32.0/20"]     # CIDR blocks for the public subnets
private_subnet_cidrs = ["10.0.128.0/20", "10.0.144.0/20", "10.0.160.0/20"] # CIDR blocks for the private subnets
availability_zones   = ["us-east-1a", "us-east-1b", "us-east-1c"]
instance_type        = "t2.micro"
custom_ami_id        = "ami-0ca2b2f5618ba7cc7"
key_pair_name        = "keypair"
application_port     = 8080
database_port        = 5432
db_username          = "csye6225"
db_password          = "csye6225"
zone_id              = "<zone_id>"
subdomain_name       = "<subdomain_name>"
aws_account_id       = <aws_account_id>
DOMAIN               = "<domain_name>"
MAILGUN_API_KEY      = "<mailgun_api_key>"
```

## Assignmetnt 9

`terraform.tfvars` 
```
region               = "us-east-1"
vpc_cidr             = "10.0.0.0/16"                                       # CIDR block for the VPC
public_subnet_cidrs  = ["10.0.0.0/20", "10.0.16.0/20", "10.0.32.0/20"]     # CIDR blocks for the public subnets
private_subnet_cidrs = ["10.0.128.0/20", "10.0.144.0/20", "10.0.160.0/20"] # CIDR blocks for the private subnets
availability_zones   = ["us-east-1a", "us-east-1b", "us-east-1c"]
instance_type        = "t2.micro"
custom_ami_id        = "ami-0ca2b2f5618ba7cc7"
key_pair_name        = "keypair"
application_port     = 8080
database_port        = 5432
db_username          = "csye6225"
db_password          = "csye6225"
zone_id              = "<zone_id>"
subdomain_name       = "<subdomain_name>"
aws_account_id       = <aws_account_id>
DOMAIN               = "<domain_name>"
MAILGUN_API_KEY      = "<mailgun_api_key>"
ssl_certificate_arn  = "<ssl_certificate_arn>"
```

Command to import the certificate:
Reference: https://www.namecheap.com/support/knowledgebase/article.aspx/9592/2290/generating-a-csr-on-amazon-web-services-aws/

1.  Generate the key: ```sudo openssl genrsa -out private.key 2048```
2.  Create CSR: ```sudo openssl req -new -key private.key -out csr.pem```
3.  See the CSR: ```cat csr.pem```
4.  See the Private Key: ```sudo cat private.key```
5.  Download the SLL Details from namecheap SSL Certificates
6.  Add the SSL Certificate to AWS Certificate Manager

```
aws acm import-certificate 
    --certificate file://Certificate.pem 
    --certificate-chain file://CertificateChain.pem 
    --private-key file://PrivateKey.pem
```
