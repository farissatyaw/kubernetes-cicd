# Kubernetes Example

This repo consist only the service files, and the CI part of the service as well as the kubernetes manifest. To fully deploy the service, we need another repo containing the "infra stuffs" to deploy. It needs flux and ALB controller (assuming its deployed on AWS) to deploy this and be able to deploy it fully

## Infra Dependencies

This is assuming we utilize flux and ALB Controller in AWS. Flux will be responsible as the GitOps operator to deploy the whole thing, and ALB controller will be responsible to create the load balancer, and the load balancer will be resposnsible redirecting the traffic to each respective service

Here is a simple image describing it.

## Explanation on CI

The CI currently only triggers when push to master branch, there should be improvement to be able trigger on pull request to verify the change, and build feature branch.

The build job only triggers if there are change inside the respective folder and in app folder, that contains thje source code of the application, and will push to my docker repo
