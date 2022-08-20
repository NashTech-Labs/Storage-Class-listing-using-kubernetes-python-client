### Install Kubernetes Python Client:

`git clone --recursive https://github.com/kubernetes-client/python.git cd`

`cd python`

`python setup.py install`

### Installation from pip:

`pip install kubernetes`

### Listing Storage Class in your cluster using python

For Storage Class, we use StorageV1Api class from client module.

Authentication to the Kubernetes Python Client in minikube is done by:

`config.load_kube_config()`

### Authentication to the Kubernetes Python Client in other cluster is done by: 

`configuration.api_key = {"authorization": "Bearer" + bearer_token}`

We will use here the Bearer Token which enable requests to authenticate using an access key.

In get_sc.py file we have to provide our cluster details for listing storage classes:


Give your cluster details:
```
cluster_details={
        "bearer_token":"<Your_cluster_bearer_token>",
        "api_server_endpoint":"<Your_cluster_IP>"
    }
```

### Running the File:
```
python3 get_sc.py
```

You will get the list of Storage class inside your cluster.