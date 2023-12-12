# voting-app
Voting app based on docker samples deployed on K8s

Assignment is based on one of the sample application provided by Docker

https://github.com/dockersamples/example-voting-app

A front-end web app in Python which lets you vote between two options
A Redis which collects new votes
A .NET worker which consumes votes and stores them in Postgres DB
A Postgres database backed by a K8s PVC
A Node.js web app which shows the results of the voting in real time