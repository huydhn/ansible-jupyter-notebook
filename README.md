# Ansible jupyter-notebook
An Ansible role to setup a Jupyter notebook, rstudio, and various stuffs. This
currenly supports only Centos 7.

Usage
-----
Installing Jupyter and RStudio locally:

```
ansible-playbook -i inventory/example jupyter.yml --become-method sudo

# The default password is `changeme'
ansible-playbook -i inventory/example jupyter.yml --become-method sudo -e 'jupyter_notebook_password=mysecret'
```

Installing Jupyter and RStudio on an Amazon EC2 instance with tag
Name=jupyter-notebook:

```
ansible-playbook -i inventory/aws jupyter.yml --become-method sudo

# The default password is `changeme'
ansible-playbook -i inventory/aws jupyter.yml --become-method sudo -e 'jupyter_notebook_password=mysecret'
```

Running the role with an Amazon EC2 instance requires the following
Python packages:

```
pip install boto boto3
```
