# Sample Voting Application
Voting app based on docker [samples](https://github.com/dockersamples/example-voting-app). It's a simple distributed application running across multiple services.

K8s manifests have been created to deploy the application on kubernetes cluster.


## Architecture
* A front-end web app in Python which lets you vote between two options
* A Redis which collects new votes
* A .NET worker which consumes votes and stores them in Postgres DB
* A Postgres database backed by a K8s PVC
* A Node.js web app which shows the results of the voting in real time

## Benifits
1. Scalable: Current design allows the services to horizontally scale
2. Persistence: Data persists restarts.

## Challenges
1. Multiple LBs required if there's no ingress controller. An ingress controller can be deployed on the cluster and configure it using ingress resources to route traffic and avoid usage of multiple services of type Load Balancer.

## Configuration Repository
https://github.com/abhinaybyrisetty/voting-app