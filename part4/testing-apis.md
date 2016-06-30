# gRPC Testing APIs

## Chef Group

Usage: `docker run -dP apibricks/chefgroup-test-grpc-api`

How the container image was built:

    git clone https://github.com/tfreundo/gRPC-API-Tester.git chefgroup-test-grpc-api
    cd chefgroup-test-grpc-api/docker-testapi
    docker build -f Dockerfile-testgrpcserver -t apibricks/chefgroup-test-grpc-api .
    docker push apibricks/chefgroup-test-grpc-api



## Puppet Group

**Please send me the link to the repo where you stored your gRPC testing API.**



## SaltStack Group

There seem to be two alternative gRPC testing APIs:

* https://github.com/Helmsen/gRPC-Adapter/tree/master/ContainerGrpcServerSupportedSpec
* https://github.com/Helmsen/gRPC-Adapter/tree/master/ContainerGrpcServerFullSpec

Unfortunately, both Dockerfiles are not self-contained, so a simple `docker build ...` and `docker run ...` is not possible.
Please add required statements to the Dockerfiles to make them self-contained:

    EXPOSE ... # the port your API is listening
    VOLUME /api
    CMD ...

**Please fix!**



## Ansible Group

Usage: `docker run -dP apibricks/ansiblegroup-test-grpc-api`

How the container image was built:

    git clone https://github.com/hubot-grpc/testing-grpc.git ansiblegroup-test-grpc-api
    cd ansiblegroup-test-grpc-api
    docker build -t apibricks/ansiblegroup-test-grpc-api .
    docker push apibricks/ansiblegroup-test-grpc-api
