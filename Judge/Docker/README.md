# Run container automatically with compose
## Build and run container:
```sh
docker compose up
```
>Note: The entrypoint for the Docker container, defining the sequence of commands to be executed, is configured in the **docker-compose.yaml** file as follows:
```yaml
entrypoint: ["/bin/bash", "-c", "./calibreitor.sh fatorial && ./build-and-test.sh c jorge.c fatorial"]
```
>This configuration specifies that when the container starts, it will **execute calibreitor.sh with the fatorial argument** followed by **build-and-test.sh with the specified arguments (c jorge.c fatorial)**. Adjust the entrypoint command in the docker-compose.yml file as needed for **your specific use case**.

# Running Manually(for tests)

## Build Image

```sh
docker image build -t judge_image -f Dockerfile_Judge .
```

## Access Container Terminal

```sh
docker container run -it --privileged judge_image /bin/bash
```

```sh
docker container exec -it judge /bin/bash
```
# Docker Runnning Test Example: <span style="color:red"> * -> manual while remap userns are not configured*</span>
## Calibreitor 
```sh
./calibreitor.sh fatorial
```

## Build And Test
```sh
./build-and-test.sh c jorge.c fatorial
```
