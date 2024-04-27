# Table of Contents

  1. [Title](#Title)
  2. [Details](#Details)
  3. [Installation](#Installation)
  4. [Benefits](#Benefits)
  5. [Licenses](#Licenses)
  6. [Contributions](#Contributions)
  7. [Github](#Github)
  8. [Email](#Email)
  
# C2 Nginx Redirector Container

# Details

### Overview

The project aims to simplify the process of setting up a Command and Control (C2) Nginx Redirector within a Docker container. By automating most of the setup process, it enables users to quickly deploy and configure multiple redirectors for various purposes such as network testing, exercise environments, or redirection of web traffic.

### Features

* Automated Docker Image Creation:
The project provides scripts to automate the creation of a Docker image tailored for running the Nginx Redirector.
* Efficient Directory Structure Setup: Users can utilize provided bash scripts to swiftly create directories within /var/www/redirectors, where each directory represents a single redirector. This directory serves as the home for specific details and files associated with the redirector.
* Container Management Scripts: The project includes scripts for creating and starting the Docker container, streamlining the management of the redirector instances.
* WireGuard Integration: To enhance versatility, the container supports the addition of WireGuard client configurations. This feature allows users to seamlessly attach the redirector to a test or exercise environment for comprehensive network testing scenarios.

# Installation
Pull Project from my GitHub and save it in a directory such as `/opt`
```bash
sudo git clone https://github.com/CyberThulhu22/Docker-Projects.git
```

Change into the Directory for Nginx C2 Redirector
```bash
cd ./Docker-Projects/C2-Nginx-Redirector
```

Run Installation script
Note: This will install Docker and Build the Docker Image (redirector:nginx) for you.
```bash
bash 0_install_requirements
```


There is a Script to help with installation that currently uses the package manager [apt](https://manpages.ubuntu.com/manpages/noble/en/man8/apt.8.html) to install.

The goal is to expand this script to automate installation on various linux hosts using different package managers. For now follow the official documentation to install docker to ensure consistency and properly working mechanics.
Ref: [Docker Docs](https://docs.docker.com/engine/install/)

# Benefits
The project offers several benefits that streamline the process of setting up and managing Nginx Redirectors within Docker containers:

1. Automation: The automation provided by the project reduces manual intervention, saving time and effort in setting up and configuring Nginx Redirectors. Users can quickly deploy multiple redirectors without the need for extensive manual configuration.
2. Consistency: With predefined scripts for creating directories and managing containers, the project ensures consistency across redirector setups. This consistency minimizes the chances of configuration errors and ensures uniformity in deployment.
3. Efficiency: By providing efficient bash scripts for directory creation and container management, the project enhances efficiency in the setup process. Users can perform tasks such as creating redirector directories and starting containers with just a few simple commands.
4. Versatility: The project's support for WireGuard integration expands its versatility, allowing users to attach redirectors to test or exercise environments seamlessly. This flexibility enables comprehensive network testing scenarios and facilitates integration with various environments.
5. Scalability: Docker's containerization technology allows for easy scaling of redirector instances as needed. Users can rapidly spin up new containers to accommodate changing requirements or workload demands, enhancing scalability and adaptability.
6. Isolation and Security: Docker containers provide isolation between applications and the host system, enhancing security by reducing the attack surface. The project leverages Docker's security features to ensure a secure environment for running Nginx Redirectors.
7. Portability: Docker containers are portable and can be easily moved or deployed across different environments, regardless of the underlying infrastructure. This portability ensures consistency and compatibility, making it easier to deploy redirectors across diverse environments.

Overall, the project's benefits include automation, consistency, efficiency, versatility, scalability, security, and portability, all of which contribute to a streamlined and effective process for setting up and managing Nginx Redirectors within Docker containers.

# Licenses
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Contributions
None

## Contributing
Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

# Github
CyberThulhu

# Email
CyberThulhu22@gmx.com
  
