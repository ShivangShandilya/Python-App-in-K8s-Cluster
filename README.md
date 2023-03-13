# Python-App-in-K8s-Cluster


## About the Project

Creating a hello world API with Python using FastAPI, bundle it up as a container image, and then deploy it to a Kubernetes cluster on Amazon Web Services (AWS)!

### Built With

- [FastAPI](https://fastapi.tiangolo.com/)

- [Docker](https://www.docker.com/)

- [Kubernetes](https://kubernetes.io/)
 
- [AWS](https://aws.amazon.com/free/?trk=14a4002d-4936-4343-8211-b5a150ca592b&sc_channel=ps&s_kwcid=AL!4422!3!453325184782!e!!g!!aws&ef_id=Cj0KCQjwk7ugBhDIARIsAGuvgPYe-svQVqVJaGT1aJDi_hLEk2jiaFo4dV8HeDyc263XZs3zp7H4JQUaAuboEALw_wcB:G:s&s_kwcid=AL!4422!3!453325184782!e!!g!!aws&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

## Why use FastAPI??

FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.7+ based on standard Python type hints.

The key features are:

- Fast: Very high performance, on par with NodeJS and Go (thanks to Starlette and Pydantic). [One of the fastest Python frameworks available.](https://fastapi.tiangolo.com/#performance)

- Fast to code: Increase the speed to develop features by about 200% to 300%. *

- Fewer bugs: Reduce about 40% of human (developer) induced errors. *

- Intuitive: Great editor support. Completion everywhere. Less time debugging.

- Easy: Designed to be easy to use and learn. Less time reading docs.

- Short: Minimize code duplication. Multiple features from each parameter declaration. Fewer bugs.

## Getting Started

- <b>First we create a virtual environment</b>

```
python3 -m venv ./venv
```

The module used to create and manage virtual environments is called venv. venv will usually install the most recent version of Python that you have available. If you have multiple versions of Python on your system, you can select a specific Python version by running python3 or whichever version you want.

- <b>Installing packages</b>

```
pip install fastapi
```

```
pip install uvicorn
```
FastAPI is the framework you’ll use to build your API, and Uvicorn is the server that will use the API you build to serve requests.

- <b>Make a basic FastAPI file</b>

If you don't know how to make one, just copy the one from repository and just like that, you have a fully functional API application with some best practices like automatic documentation and serialization built in.

<p align = "center">
<img src = "https://user-images.githubusercontent.com/101946115/224777832-5a2728f5-3e75-4863-a26c-4eb5d5c28358.png" />
</p>

This code defines your application, but it won’t run on itself if you call it with python directly. To run it, you need a server program. In the steps above, you already installed Uvicorn. That will be your server.

- <b>Create and build a simple Dockerfile</b>

```
docker build -t {your preferred name} .
```

- <b>Create a repository at DockerHub and push your image there</b>

- <b>Log in to your AWS account and via its EKS service, create a Kubernetes Cluster</b>

- <b>Create a simple demployment and service file for the cluster and appply them using following command:</b>

```
kubectl apply -f .
```

- <b>Now to deploy your application on cluster</b>

```
kubectl port-forward {any running pod name} 8080:80
```

## Usage

The primary goal of this project is to help you learn how to deploy an application on Kubernetes cluster via a CSP
