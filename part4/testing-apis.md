# gRPC Testing APIs

## Chef Group

Usage: `docker run -dP apibricks/chefgroup-test-grpc-api`

How the container image was built:

    git clone https://github.com/tfreundo/gRPC-API-Tester.git chefgroup-test-grpc-api
    cd chefgroup-test-grpc-api/docker-testapi
    docker build -f Dockerfile-testgrpcserver -t apibricks/chefgroup-test-grpc-api .
    docker push apibricks/chefgroup-test-grpc-api



## Puppet Group

Usage: `docker run -dP apibricks/puppetgroup-test-grpc-api`

How the container image was built:

    git clone https://github.com/shruthikuki/CloudLab-IAAS-UniStuttgart-Part3-gRPCTest puppetgroup-test-grpc-api
    cd puppetgroup-test-grpc-api/Docker
    docker build -t apibricks/puppetgroup-test-grpc-api .
    docker push apibricks/puppetgroup-test-grpc-api



## SaltStack Group

Usage: `docker run -dP apibricks/saltgroup-test-grpc-api`

How the container image was built:

    git clone https://github.com/Helmsen/gRPC-Adapter.git saltgroup-test-grpc-api
    cd saltgroup-test-grpc-api/ContainerGrpcServer
    docker build -t apibricks/saltgroup-test-grpc-api .
    docker push apibricks/saltgroup-test-grpc-api



## Ansible Group

Usage: `docker run -dP apibricks/ansiblegroup-test-grpc-api`

How the container image was built:

    git clone https://github.com/hubot-grpc/testing-grpc.git ansiblegroup-test-grpc-api
    cd ansiblegroup-test-grpc-api
    docker build -t apibricks/ansiblegroup-test-grpc-api .
    docker push apibricks/ansiblegroup-test-grpc-api
