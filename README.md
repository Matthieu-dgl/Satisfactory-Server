# Satisfactory-Server

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A Docker-based dedicated server setup for [Satisfactory](https://www.satisfactorygame.com/), using the [`wolveix/satisfactory-server`](https://github.com/wolveix/satisfactory-server) image.

## Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. Clone this repository:

   ```bash
   git clone https://github.com/Matthieu-dgl/Satisfactory-Server.git
   cd Satisfactory-Server
   ```

2. Edit `docker-compose.yml` and replace `PATH/TO/YOUR/STORAGE` with the path where you want to store server data (e.g. `./satisfactory-data:/config`).

3. Start the server:

   ```bash
   docker compose up -d
   ```

4. Check the logs:

   ```bash
   docker compose logs -f
   ```

## Configuration

| Environment Variable | Default | Description |
|---|---|---|
| `MAXPLAYERS` | `8` | Maximum number of players allowed |
| `PGID` | `1000` | Group ID for the server process |
| `PUID` | `1000` | User ID for the server process |
| `ROOTLESS` | `false` | Run the container without root privileges |
| `STEAMBETA` | `false` | Use the Steam beta branch |

## Ports

| Port | Protocol | Description |
|---|---|---|
| `7777` | UDP/TCP | Game traffic |
| `8888` | TCP | Server management API |

## License

This project is licensed under the [MIT License](LICENSE).
