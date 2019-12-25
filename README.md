# pycho

A simple OpenFaaS function that can be deployed as an echo server. As any good echo server should, the HTTP body of the request is returned as the response. Additionally,
the request body is logged to stdout.

The goal is that these should be really easy to deploy and verify a deployment of OpenFaaS.

The Quart based function also provides an example of a Python function using `async/await`.


## Deploying

The Flask based echo function can be deployed using
```sh
faas-cli deploy --name pycho --image theaxer/pycho:latest --fprocess='python index.py'
```

The Quart based echo function can similarly be deployed using
```sh
faas-cli deploy --name pycho-async --image theaxer/pycho-async:latest --fprocess='python index.py'
```

## Development
The project can quickly be setup using conda,

```sh
conda env create -f environment.yaml
```



