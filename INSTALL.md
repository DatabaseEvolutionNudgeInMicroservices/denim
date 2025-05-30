# DENIM

## Installation

### Prerequisites

1. Docker:

- Linux: [Install Docker Engine](https://docs.docker.com/engine/install/)
  or [Install Docker Desktop](https://docs.docker.com/desktop/setup/install/linux/).
- Windows: [Install Docker Desktop](https://docs.docker.com/desktop/setup/install/windows-install/).
- MacOS: [Install Docker Desktop](https://docs.docker.com/desktop/setup/install/mac-install/).

### Launching

The following method aims to launch the complete and entire architecture in one shot thanks to Docker and docker-compose.

#### Launching the architecture with Docker

You can launched the entire application in one shot thanks to the following command:

```bash
docker-compose up
```

⚠️ This command must be executed at the location of the `docker-compose.yml` file and have to be run as with the right privileges (administrator).

The overall deployment [`docker-compose.yml`](docker-compose.yml) file corresponds to the deployment schema illustrated in the [Architecture](README.md#architecture) section of the [`README.md`](README.md) file. You can adapt ports, hosts, and networks in regard to your needs.
