# mlflow-tracking-server
Docker compose with mlflow lockal tracking server


Repository based on repo:
https://github.com/PacktPublishing/Practical-Deep-Learning-at-Scale-with-MLFlow/tree/main/chapter03/mlflow_docker_setup

python:3.9 mlflow==2.4.1

## Set up a local full-fledged MLflow tracking and registry server with MySQL as backend storage and MinIO as the artifact store
#### The mlflow docker setup is based on `https://github.com/sachua/mlflow-docker-compose` with updates on latest versions of images of nginix and minio and python version to 3.8. Also fixed bugs for creating buckets using minIO.
   1. Run `bash start_mlflow.sh` to start the mlflow server
      
      a) You must have docker running in your local environment in order to successfully run the docker-compose command
      
      b) Please refer to https://docs.docker.com/engine/install/ to install either Docker Desktop or a linux distr of docker. 
      
      c) Once the docker is installed, start it so it is running in the background.
   2. See the MLflow server UI at `http://localhost`
   3. See the object store (minIO, a multi-cloud object store) UI at `http://localhost:9000`
   4. When you are done, run `bash stop_mlflow.sh` to stop the local mlflow server
