Launch EC2 Instance
Log in to AWS Management Console:

Go to the AWS Console.
Navigate to EC2 Dashboard:

Find and select EC2 from the AWS services.
Launch Instance:

Click on the Launch Instances button.
Configure Instance Settings:

Name: Provide a meaningful name (e.g., UbuntuServer).
AMI (Amazon Machine Image): Select Ubuntu Server 22.04 LTS or the version you prefer.
Instance Type: Choose an instance type (e.g., t2.micro for free tier eligibility).
Key Pair:
If you have an existing key pair, select it.
If not, create a new key pair, download it (.pem file), and save it securely.
Network Settings:
Ensure SSH (port 22) is open in the security group rules.
Optionally, restrict the source IP to your own for better security.
Storage: Configure as needed (e.g., 8 GiB for general usage).
Launch the Instance:

Review the settings and click Launch Instance.
Wait for Instance to Initialize:

Go to the Instances page and wait until the instance's status is Running.
CONNECT TO THE INSTANCE VIA SSH
Locate Instance Details:

Find your instance in the EC2 dashboard.
Note the Public IPv4 Address or Public DNS.
Set Up Your Environment:

Ensure you have an SSH client installed:
Linux/macOS: Use the built-in ssh command.
Windows: Use PowerShell, PuTTY, or Windows Subsystem for Linux (WSL).
Connect to the Instance:

Open a terminal or command prompt.
Navigate to the directory where your .pem file is stored.
run the following command
ssh -i "path_to_your_key.pem" ubuntu@your_instance_public_ip
