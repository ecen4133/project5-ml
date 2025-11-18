# P5 Environment Setup

This project uses Docker for a consistent development environment.

## Prerequisites

Create a Virtual Environment:

`python3 -m venv ./venv`

And activate it:

`source ./venv/bin/activate`

Then, install the necessary libraries:

`pip install --no-cache-dir -r ./requirements.txt`


## Optional: Using Docker

We also provide the docker container we'll use for grading if you want to use that
(though the above virtual environment should be sufficient).

To use this, you'll need to install [Docker Desktop](https://www.docker.com/products/docker-desktop) and ensure it's running.

You can test if you have Docker installed correctly by running `docker run -it --rm hello-world`

### Option 1: VS Code Dev Container

For VS Code users, you can open the project inside a dev container:

1. Install the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
2. Clone and open the project in VS Code
3. Click **"Reopen in Container"** when prompted (or `Ctrl+Shift+P`(Windows/Linux)/`Cmd+Shift+P`(Mac) → "Dev Containers: Reopen in Container")

The first time you do this, it may take a few minutes to download and build the container.

And that's it! You should be able to see that your environment has changed to "Dev Container" on the bottom left. You can run the project commands in the terminals tab and install your favorite VS Code extensions by clicking "Install in Dev Container" button on the extensions tab.

The dev container configuration may also work on other editors that supports dev containers (such as JetBrains). Check your editor's documentation for instructions.

### Option 2: Command Line Docker

If you use an editor that does not support dev containers, you can clone the project and edit locally.

When you want to run any commands and test the project, run this from your project directory:

```bash
docker run -it --rm -v ./:/workspace -w /workspace ghcr.io/ecen4133/project5:latest
```

The first time you do this, it may take a few minutes to download and build the container.

Your project will be mounted at `/workspace` and you should be able to run the commands used in the project.
