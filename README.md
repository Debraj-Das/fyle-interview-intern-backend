# Fyle Backend Challenge

## Installation

1. Fork this repository to your github account
2. Clone the forked repository and proceed with steps mentioned below

### Install requirements

```bash
virtualenv env --python=python3.8
source env/bin/activate
pip install -r requirements.txt
```
### Reset DB

```bash
export FLASK_APP=core/server.py
rm core/store.sqlite3
flask db upgrade -d core/migrations/
```
### Start Server

```bash
bash run.sh
```
### Run Tests

```bash
pytest -vvv -s tests/

# for test coverage report
# pytest --cov
# open htmlcov/index.html
```

## Building and Running this Application using Docker

### Prerequisites
Ensure Docker is installed on your machine. You can download it from [Docker's official website](https://www.docker.com/products/docker-desktop).

### Build Docker Image
```bash
docker build -t latest285d0b665dcefb2be5554a399 .
```

### Run Docker Container
```bash
docker run -d -p 8080:8080 --name my-application-container latest285d0b665dcefb2be5554a399
```

### Stopping Docker Container
```bash
docker stop my-application-container
```

### Removing Docker Container
```bash
docker rm my-application-container
```

### Removing Docker Image
```bash
docker rmi latest285d0b665dcefb2be5554a399
```
