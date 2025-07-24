# DENIM

## 📣 Description

DENIM is a tool aiming to provide software developers support in downloading, reverse engineering, visualizing, and evolving microservices architecture. Further details of each goals are provided in respective repositories referenced hereafter.

This documentation repository aims to explain the overview of the tool in terms of objectives and technical details (e.g. architecture diagram, languages and technologies).

## 🪛 Technical details

### Architecture

The tool is developed itself as a microservices architecture. The architecture diagram is depicted below.

<img src="assets/architecture_diagram.svg" alt="Model" width="500px"/>

The architecture components are described below.

| Microservice        | Port  | Input | Output | Description                                                                                                                                                                                                                                                                                                                                                                   | Repository                                                                 |
| ------------------- | ----- | ----- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Web                 | :8080 | HTTP  | HTTP   | This microservice is the user interface of the tool. It interacts through HTTP requests with the user. It also communicates with other services through API requests in order to respond to user's needs according to the proposed features.                                                                                                                                  | [Web](https://github.com/DatabaseEvolutionNudgeInMicroservices/web/)                                 |
| Downloading         | :8081 | JSON  | ZIP    | This microservice aims to help the user to download, in one shot, with git, one or several microservices applications composing a microservices architecture and spread across multiple, distributed, and heterogenous repositories. According to a given JSON list of repositories links and hash as input, it returns a ZIP file containing all the architecture as output. | [Downloading](https://github.com/DatabaseEvolutionNudgeInMicroservices/downloading/)                 |
| Reverse Engineering | :8082 | ZIP   | JSON   | This microservice aims to reverse engineer, statically and dynamically, a microservices architecture in order to retrieve insights about the data access. According to a given ZIP file containing the microservices architecture as input, it returns a requested analysis report in JSON as output.                                                                         | [Reverse Engineering](https://github.com/DatabaseEvolutionNudgeInMicroservices/reverse-engineering/) |
| Visualization       | :8083 | JSON  | JSON   | This microservice aims to transform a static analysis report into visualizations. According to given a analysis report in JSON as input, it returns a one of the requested visualization model object in JSON as output.                                                                                                                                                      | [Visualization](https://github.com/DatabaseEvolutionNudgeInMicroservices/visualization/)             |
| Evolution           | :8084 | JSON  | JSON   | This microservice aims to retrieve, based on an analysis report, some evolution insights. According to a given analysis report in JSON as input, it returns a one of the requested evolution insight in JSON as output.                                                                                                                                                       | [Evolution](https://github.com/DatabaseEvolutionNudgeInMicroservices/evolution/)                     |

Comments:

- Each microservice have a `Dockerfile` file and a `docker-compose.yml` file.
- ⚠️ Port exposed in respective `Dockerfile` files of each repository corresponds to the concerned technology's default one. In addition, each respective `docker-compose.yml` file of each repository maps by default this same default port. ⚠️ Pay attention that for the complete deployment, it is required to use different ports for each service. The overall `docker-compose.yml` file described in the [Deployment](#deployment) section proposes an example according to the port illustrated in the diagram above.

### Deployment

See [INSTALL file](INSTALL.md).

### Technologies

As recommended in microservices architectures, each microservice motivates their own technology choices. See respective repositories for further details.

### Libraries

As recommended in microservices architectures, each microservice motivates their own libraries choices. See respective repositories for further details.

### Tools

As recommended in microservices architectures, each microservice motivates their own tool choices. See respective repositories for further details.

## 🤝 Contributing

Contributions guidelines are described in each repositories. See respective repositories for further details.
