# Vagrant

Vagrant is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past.

# Why Vagrant?

Vagrant is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past.

To achieve its magic, Vagrant stands on the shoulders of giants. Machines are provisioned on top of VirtualBox, VMware, AWS, or any other provider. Then, industry-standard provisioning tools such as shell scripts, Chef, or Puppet, can automatically install and configure software on the virtual machine.

## Installation
```bash
sudo apt-get install virtualbox
sudo apt-get install vagrant
sudo apt-get update
```

## Usage

```bash
cd Simple-Vagrant-Scripts/Single-Vm
vagrant init
vagrant up
```

## Essential Commands
```bash#
#Login to Vagrant Cloud
vagrant cloud auth login

#check box status
vargant stauts

#full stauts
vagrant global-status

#Box list. In this Current tutorials, we already install hashicorp/bionic64
vagrant box list

#login to vagrant box
vagrant ssh <box-name>

#stop vagrant box
vagrant halt <box-name>

#stop vagrant box with one command
vagrant global-status | grep virtualbox | cut -c 1-9 | while read line; do echo $line; vagrant halt $line; done;

#Delete Vm
vagrant destory '<box-id> or <box-name>'

#Delete box
vagrant remove hashicorp/bionic64
```
