# Overview

This template will create a Basic RDS Instance that is publicly accessible.

# Validate the Basic RDS Instance Template

`aws cloudformation validate-template --template-body file://basic_aurora_crossregion_replica.yaml`

# Launch the Basic RDS Instance Stack

`random_password=$(openssl rand -base64 12)`
`aws cloudformation create-stack --stack-name BasicAuroraReadReplica --template-body file://basic_aurora_crossregion_replica.yaml`

# Update the Basic RDS Instance Stack

`random_password=$(openssl rand -base64 12)`
`aws cloudformation update-stack --stack-name BasicAuroraReadReplica --template-body file://basic_aurora_crossregion_replica.yaml`
