### "Standardized" interface between gRPC API containers and API adapter containers

* Each gRPC API container *must* provide the following file: `/api/main.proto`

* The `/api` directory is a shared Docker volume. It is provided by the gRPC API container and used by the API adapter container. The API adapter container loads the `/api/main.proto` file to communicate with the gRPC API container.

* The `/api/main.proto` file is the *only* required file. Therefore each API adapter must work properly based on this file without any additional metadata.

* The `/api` directory *can* optionally contain additional files such as metadata, which may be read and considered by certain API adapters.

* The `/api/main.proto` file *must* follow the Protocol Buffers specification version 3 (proto3). Therefore each API adapter *must* understand all proto3 features:
  * https://developers.google.com/protocol-buffers/docs/reference/proto3-spec
  * https://developers.google.com/protocol-buffers/docs/proto3

* The environment variables `API_HOST` (IP address or hostname) and `API_PORT` (port number) *must* be provided to the API adapter, so the adapter can connect to the gRPC API.

* The environment variable `API_PROTO_PATH` *can* optionally be provided to the API adapter to load another proto3 file instead of the default (`/api/main.proto`).
