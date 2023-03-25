# cloud-devops

Reference

[Add a persist_to_workspace block](https://circleci.com/docs/workspaces/)

list the EC2 instance and save the IP address to the inventory file:

aws ec2 describe-instances --query 'Reservations[*].Instances[*].PublicIpAddress' --filters "Name=tag:Name,Values=project2server" --output text >> inventory
