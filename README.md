# pwn_docker_setup
Add pwn-raleted tools automatically to docker's container 
___
* Build the original `Dockerfile`:
```c
docker build -t <pwn_challenge> .
```

* Create `Dockerfile.debug`: (to extends the original built Image)
  
  [Dockerfile.debug](https://github.com/geetHup9n0L/pwn_docker_setup/blob/main/Dockerfile.debug)

* Build the debug image:
```c
docker build -t <pwn_dbg_challenge> -f Dockerfile.debug .
```
* Run the debug container:
```c
docker run -it \
  --cap-add=SYS_PTRACE \
  --security-opt seccomp=unconfined \
  --name <pwn_dbg_container> \
  <pwn_dbg_challenge> \
  /bin/bash
```
* To delete container:
```c
docker rm -f <pwn_dbg_container>
```

**Notes:** change value `<name>` to your own preferred names
