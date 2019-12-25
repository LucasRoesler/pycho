# pycho

A simple OpenFaaS function that can be deployed as an echo server. As any good echo server should, the HTTP body of the request is returned as the response. Additionally,
the request body is logged to stdout.


## Deploying

```sh
faas-cli deploy --name pycho --image theaxer/pycho:latest --fprocess='python index.py'
```

## Development
The project can quickly be setup using conda,

```sh
conda env create -f environment.yaml
```



