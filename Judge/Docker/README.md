# Run Container
## Build and run container:
```sh
docker compose up
```

## In other terminal, enter in container
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
