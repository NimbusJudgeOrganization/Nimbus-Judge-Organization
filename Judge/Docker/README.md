# Run Container
## Build and run container:
    ```
    docker compose up
    ```

## In other terminal, enter in container
    ```
    docker container exec -it judge /bin/bash
    ```
# Docker Runnning Test Example: <span style="color:red"> * -> manual while remap userns are not configured*</span>
## Calibreitor 
```
./calibreitor.sh fatorial
```

## Build And Test
```
./build-and-test.sh c jorge.c fatorial
```
