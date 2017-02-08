# _*_ mode: ruby _8_
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
 config.vm.provider :aws do |aws, override|
   aws.access_key_id = ENV['AWS_KEY']
   aws.secret_access_key = ENV['AWS_SECRET']
   aws.keypair_name = ENV['AWS_KEYNAME']
   aws.ami = "ami-1c47407f"
   aws.region = "ap-southeast-2"
   aws.instance_type = "t2.micro"
   aws.security_groups = "MyWebDMZ"
   aws.tags = {
   'Name' => 'efx-test-dev1'
   }

   override.vm.box = "dummy"
   override.ssh.username = "ec2-user"
   override.ssh.private_key_path = ENV['AWS_KEYPATH']
 end
end


OR




# _*_ mode: ruby _8_
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
 config.vm.provider :aws do |aws, override|
   aws.access_key_id = ENV['AWS_KEY']
   aws.secret_access_key = ENV['AWS_SECRET']
   aws.keypair_name = ENV['AWS_KEYNAME']
   aws.ami = "ami-98d9ddfb"
   aws.region = "ap-southeast-2"
   aws.instance_type = "t2.micro"
   aws.security_groups = "shared-provisioning-nonprod-sg"
   aws.use_iam_profile= "EFXSlaveProvisioningInstanceProfile"
   aws.subnet_id= "subnet-d9a351bd"
   aws.tags = {
   'Name' => 'efx-test-dev1',
   'CostCentre' => 'V_EFXSales'
   }
   override.vm.box = "dummy"
   override.ssh.username = "ec2-user"
   override.ssh.private_key_path = ENV['AWS_KEYPATH']
 end
end
~
