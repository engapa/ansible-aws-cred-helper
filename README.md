ansible-aws-cred-helper
=======================
An ansible role to configure aws ecr credential helper

Based on :

 - https://github.com/awslabs/amazon-ecr-credential-helper
 - https://hub.docker.com/r/pottava/amazon-ecr-credential-helper/

Requirements
------------

An AWS account with ECR.

Role Variables
--------------

- image_name: pottava/amazon-ecr-credential-helper (image container)
- image_version: docker image version (latest)
- aws_creds_type: source of aws credentials (one of env or file)
- aws_directory: local aws directory ($HOME/.aws)
- docker_directory: local docker directory ($HOME/.docker)

Example Playbook
----------------

Here you are an example

    - hosts: servers
      roles:
      - role: ansible-aws-ecr-creds
        aws_ecr_registry: probando.dkr.ecr.eu-west-1.amazonaws.com
        aws_access_key_id: 12345623412321
        aws_secret_access_key: 67891011123654


Author Information
------------------

engapa@gmail.com
