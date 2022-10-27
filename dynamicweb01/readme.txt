launch an ec2 with name dynamic-web-app, aws linux 2 ami, t2.micro, set security group with ssh anywhere ipv4, http anywhere ipv4, create a keypair
connect to your instance via ssh using vscode where you have your keypair
change to root user "sudo su"
run the following code to install apache and lamp server with mariadb
yum update -y
amazon-linux-extras install -y lamp-mariadb10.2-php7.2 php7.2
yum install -y httpd mariadb-server
yum info package_name
systemctl start httpd
systemctl enable httpd
systemctl is-enabled httpd
create an s3 bucket with a unique name
updload the dynamic website script u downloaded from (https://startbootstrap.com/previews/freelancer) to s3
remember to set your aws cli programatic access
cd /var/www/html
aws s3 cp s3://<your bucket name> ./ --recursive
copy your public ip or public dns name to your browser.
