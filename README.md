# AWS-TerraformScripts
 My First Script, Create a Simple EC2 Instance - ec2create.tf
Notes:

-terraform init - initialize workspace

- terraform fmt - formats code according to best practice

-terraform Apply - Yes to confirm

-terraform.tfstate - very important file, keeps track of the ID's of created

resource so that Terraform knows what it is managing

-terraform show - inspect current state





######################Terraform State##########################

1. Determine how state is performed
2. Default is stored on local disk
3. Create 3 bucket .ie 
aws s3api create-bucket --bucket terraformstatebucket141
4. Create .tf file for the state
{
Required_version = ">= 0.12.0"
Backend "s3"{
Region  = "us-east-1"
Profile = "default"
Key = "terraformstatefile" # name that state file is given when saved
Bucket = "terraformstatebucket141"
}

When you run terraform init and terraform apply it will check against the state file in 
The s3 bucket

-Deploy the Confirguration
terraform init - looks at conf file to read our provider and downloads

terraform plan - looks in current directory and checks var file

terraform plan out mybuild.tfplan

terraform apply to deploy

terraform destroy 
