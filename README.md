# Bake AMI with Ansible

blog post: *TBA*

Build Amazon AMI with [Ansible](http://www.ansible.com/).

## Quickstart

Install [Ansible](http://www.ansible.com/) and [boto](https://github.com/boto/boto):

`pip install ansible boto`

Edit `./group_vars/all.yml` to suit your configuration (`keypair` is SSH key name in AWS, `keypair_file` SSH key on the local system).

Export AWS credentials as environment variables:

```sh
export AWS_ACCESS_KEY_ID=XXX
export AWS_SECRET_ACCESS_KEY=XXX
```

run the below command to bake Amazon AMI:

```sh
ansible-playbook -i inventory -vvvv bake-aws-ami.yml
```
