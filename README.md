# kamalgo

A minimal Go web server for testing [Kamal](https://kamal-deploy.org/) deployments.

## Overview

This project provides a simple "Hello World" web server written in Go, designed specifically for testing and learning Kamal deployment workflows.

## Features

- Lightweight Go HTTP server
- Serves a simple "Hello World!" HTML page
- Listens on port 80
- Dockerized for easy deployment
- Pre-configured for Kamal deployments

## Running Locally

```bash
go run app.go
```

Visit `http://localhost` in your browser to see the Hello World page.

## Deploying with Kamal

### Prerequisites

- [Kamal](https://kamal-deploy.org/) installed
- Docker registry access configured
- Target server(s) configured in `config/deploy.yml`

### Deploy

```bash
# Initial setup
kamal setup

# Deploy the application
kamal deploy

# Check status
kamal app details
```

### Other Kamal Commands

```bash
# View logs
kamal app logs

# Restart the application
kamal app restart

# Remove the application
kamal app remove
```

## Project Structure

```
.
├── app.go              # Simple Go web server
├── Dockerfile          # Container image definition
├── config/
│   └── deploy.yml      # Kamal deployment configuration
└── .kamal/
    └── hooks/          # Kamal deployment hooks
```

## License

This is a test project for Kamal deployment experimentation.
