FROM python:3.12-slim-bullseye

ENV POETRY_VERSION 1.4.1
<<<<<<< HEAD
<<<<<<< HEAD
RUN apt update && apt install net-tools 
=======

>>>>>>> parent of 9ed50d1 (适配国产机器)
=======
ENV HTTPS_PROXY http://172.27.74.185:7890

>>>>>>> parent of 76754ea (调试dockerfile)
# Install system dependencies
RUN pip install "poetry==$POETRY_VERSION"

# Set work directory
WORKDIR /app

# Copy only requirements to cache them in docker layer
COPY poetry.lock pyproject.toml /app/

# Disable the creation of virtual environments
RUN poetry config virtualenvs.create false

RUN poetry source add mirrors https://pypi.tuna.tsinghua.edu.cn/simple/

# Install dependencies
RUN poetry install

# Copy the current directory contents into the container at /app
COPY ./ /app/
