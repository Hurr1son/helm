# helm
This repository is used to store Helm Charts.
We have one chart named `rental`. It has such templates as:
- `development.yaml`. This file creates a development with pods, assigns images to the pods, and also creates variables for the database (the value of the variables is taken from Kubernetes Secrets, which is created in Terraform at the stage of creating the infrastructure)
- `service.yaml`. The settings for traffic flow to the application are used. The service type used by ClusterIP.
- `ingress.yaml`. Provides routing of incoming traffic. Services are assigned a hostname.
