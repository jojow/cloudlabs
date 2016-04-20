### "Standardized" interface between gRPC API containers and API adapter containers

* Each gRPC API container must provide the following file: `/api/main.proto`

* The `/api` directory is a shared Docker volume; it is provided by the gRPC API container and used by the API adapter container; the API adapter container loads the `/api/main.proto` file to communicate with the gRPC API container

* The `/api/main.proto` file is the only required file; therefore each API adapter container must work properly based on this file without any additional metadata

* The `/api` directory can optionally contain additional files such as metadata, which may be read and considered by certain API adapters

* The `/api/main.proto` file contains content according to Protocol Buffers version 3

* The `/api/main.proto` file is not allowed to define a package
