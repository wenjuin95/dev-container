# dev-container

A collection of [VS Code Dev Container](https://containers.dev/) configurations for different programming languages. Each configuration provides a ready-to-use, containerised development environment so you can start coding without any manual toolchain setup.

---

## Table of Contents

- [What is a Dev Container?](#what-is-a-dev-container)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)

---

## What is a Dev Container?

A Dev Container is a Docker-based environment defined by a `devcontainer.json` file (and optionally a `Dockerfile`). VS Code (or any [Dev Containers–compatible editor](https://containers.dev/supporting)) opens your project *inside* the container, giving you:

- A consistent, reproducible environment across machines.
- Pre-installed language runtimes, tools, and VS Code extensions.
- Isolated dependencies that never pollute your host system.

---

## Prerequisites

| Tool | Minimum Version |
|------|----------------|
| [Docker Desktop](https://www.docker.com/products/docker-desktop/) (or Docker Engine on Linux) | Latest stable |
| [Visual Studio Code](https://code.visualstudio.com/) | Latest stable |
| [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) | Latest stable |

---

## Getting Started

1. **Clone this repository**

   ```bash
   git clone https://github.com/wenjuin95/dev-container.git
   cd dev-container
   ```

2. **Copy the desired container configuration into your project**

   ```bash
   # Example: use the Go container
   cp -r go/.devcontainer /path/to/your/project/.devcontainer
   ```

   Or simply open the relevant sub-folder directly in VS Code (see next step).

3. **Open the folder in VS Code**

   ```bash
   code go/   # or: code java/
   ```

4. **Reopen in Container**

   When prompted by VS Code, click **"Reopen in Container"**. Alternatively, open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`) and run:

   > **Dev Containers: Reopen in Container**

   VS Code will build the Docker image (first run only) and attach to the container. Your workspace is mounted at `/workspace` inside the container.

---
