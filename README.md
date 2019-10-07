# AWS-TerraformScripts
 My First Script, Create a Simple EC2 Instance - ec2create.tf
Notes:

-terraform init - initialize workspace

-terraform Apply - Yes to confirm

-terraform.tfstate - very important file, keeps track of the ID's of created

resource so that Terraform knows what it is managing

-terraform show - inspect current state



######################PluralSight Course##########################

-Provison Resources

-Terraform Components

-Work with variables

-Deploy the Confirguration
terraform init - looks at conf file to read our provider and downloads

terraform plan - looks in current directory and checks var file

terraform plan out mybuild.tfplan

terraform apply to deploy

terraform destroy 