provider "aws"  {
  region = "ap-south-1"
}
resource "aws_instance" "first" {
  ami           = "ami-02913db388613c3e1"
  instance_type = "t2.micro"
  key_name      = "newterraform"
}
resource "aws_instance" "second" {
  ami           = "ami-02913db388613c3e1"
  instance_type = "t2.micro"
  key_name      = "newterraform"
  provisioner "local-exec" {
        command = "echo ${aws_instance.second.private_ip} > private_hosts; echo ${aws_instance.first.private_ip} >> private_hosts"
        }
