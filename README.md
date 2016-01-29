# Bake AMI with Ansible

blog post: TBA  

## Quickstart

Install Build AMIs with [Ansible](http://www.ansible.com/) and [boto](https://github.com/boto/boto) if they are not already present system `pip install ansible boto`.

Edit `./group_vars/all.yml` to suit your configuration, `keypair` specifies your public SSH key in AWS, `keypair_file` is your SSH key on the local system.

Export AWS credentials for your user as environment variable:

```sh
export AWS_ACCESS_KEY_ID=XXX
export AWS_SECRET_ACCESS_KEY=XXX
```

bake AMI in one command:

```sh
ansible-playbook -i inventory -vvvv bake-aws-ami.yml
```
