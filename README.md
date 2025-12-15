# pwn_docker_setup
Add pwn-raleted tools automatically to docker's container 
___
Build the Debug Image:
```c
docker build -t pwn_dbg_challenge -f Dockerfile.debug .
```
Run the Debug Container:
```
docker run -it \
  --cap-add=SYS_PTRACE \
  --security-opt seccomp=unconfined \
  --name pwn_dbg_container \
  pwn_dbg_challenge \
  /bin/bash
```
