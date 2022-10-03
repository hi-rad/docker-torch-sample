# Docker Compose Sample for PyTorch with CPU

This repository contains a sample Dockerfile and a sample docker-compose file to run PyTorch using Docker.

Make sure you have installed `Docker` and `docker compose`:

- [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)
- [https://docs.docker.com/compose/](https://docs.docker.com/compose/)

The project is a basic MNIST example using PyTorch taken from [https://github.com/pytorch/examples/tree/main/mnist](https://github.com/pytorch/examples/tree/main/mnist).

## Running the project
### Running for the first time
To run the project for the first time:

1. Make a copy of `.env.example` file and name it `.env`
2. Change the port number in `.env` to your desired port
3. Open a `terminal` window
4. Change your directory to the project directory
5. Run `docker compose up --build`

The above command (step 5) first builds the container, then runs the project. It will provide a link to Jupyter Lab
### Running the project after making changes
If you are making changes to the `Dockerfile`, `docker-compose.yml`, `requirements.txt`, or `.env` files, you need to rebuild the project. To do so:

1. Open a `terminal` window
2. Change your directory to the project directory
3. Run `docker compose up --build`

If you have made changes to `.py` or `.ipynb` files, you don't need to rebuild the project, and you can simply:

1. Open a `terminal` window
2. Change your directory to the project directory
3. Run `docker compose up`

## Terminating the project
To terminate the project in the terminal:

1. Use `Ctrl + c` on Windows/Linux or `Command + c` on macOS
2. Run `docker compose down`