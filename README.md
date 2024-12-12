# Dockerfile Bug: Missing Application Source Code

This repository demonstrates a common error in Dockerfiles: forgetting to copy the application's source code into the image.  The provided `Dockerfile` attempts to run a Python script, `my_script.py`, but this script is not included in the image. This leads to a runtime error when attempting to start the container.

The solution shows how to correctly include the source code using the `COPY` instruction.

## Bug:

The `Dockerfile` in this repository attempts to install dependencies and run a python script, but fails to copy the script itself into the image.  This leads to a runtime error within the Docker container.

## Solution:

The `Dockerfile_solution` fixes the issue by correctly using the `COPY` instruction to copy the application source code (including `my_script.py`) into the image before the `CMD` instruction.