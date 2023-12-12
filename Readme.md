# Plug&Play Docker Compose for Unifi Network Application

Welcome to this repository for a seamless Plug&Play Docker Compose setup for the Unifi Network Application. This repository contains everything you need to get started with minimal setup. Simply clone this repository and run `docker compose up -d`, and you're good to go!

## Features

- **Complete Package**: Includes a Docker Compose file, a well-organized folder structure, and an initialization script. This setup is designed to be as straightforward as possible.
- **Based on "trusted sources" 🙈**: The Docker Compose is based on the docker image from [linuxserver](https://github.com/linuxserver),  leveraging the proposal by [Natan Keddem](https://github.com/natankeddem) (as seen in [this issue](https://github.com/linuxserver/docker-unifi-network-application/issues/13)).
- **Custom Enhancements**: While most of the credit goes to LSIO and Natan Keddem for their foundational work, this repository includes a few minor but crucial tweaks:
  - Synchronized database name between the script and Docker Compose.
  - Removal of an unnecessary external port for MongoDB, streamlining the setup.

## Important For Adopting Devices

The Unifi Network Application within the Docker Compose network has a different IP address than the Docker Host in the actual network. This means that the Unifi Network Application is unaware of the host's actual network IP address. To adopt devices, you need to override the "Inform host" address. This can be done by navigating to **Settings -> System -> Advanced** in the Unifi Controller UI and applying the necessary override.

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/vlorian-de/unifi-network-application-pnp
   ```

2. **Run Docker Compose**
   ```bash
   docker compose up -d
   ```

3. **Access the Unifi Controller**
   Open your browser and navigate to the Unifi Controller's web interface at https://{host}:8443.
   Follow the setup instructions to configure your network.

## Acknowledgements
A huge thanks to the team at linuxserver.io and especially to Natan Keddem for their initial work and contributions which made this repo possible.