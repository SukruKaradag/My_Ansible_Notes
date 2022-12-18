# Installation

## AWS Linux 2

```bash
sudo yum update -y
sudo amazon-linux-extras install ansible2 -y
```

## Pip

```bash
sudo pip install ansible
```

## Ubuntu

```bash
sudo apt update -y
sudo apt install -y ansible
```

# Notes


# Commands
- `/etc/ansible/host` içine makinaları ekle:
```bash
[webservers] #Control edilecek makinalar belirtilir 
weba ansible_host=44.202.112.160 ansible_user=ec2-user
webb ansible_host=44.204.69.121 ansible_user=ec2-user

[all:vars] # Kullanılacak variable'lar belirtilir. 'all:' yerine farklı gruplar yazılabilir.
ansible_ssh_private_key_file=/home/ec2-user/my_Keypam.pem

```
ansible all --list-host
ansible all -m ping