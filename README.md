# pwn_docker_setup
Add pwn-raleted tools automatically to docker's container 
___
1. Build the original `Dockerfile`:
```c
docker build -t <pwn_challenge> .
```

2. Create `Dockerfile.debug`: (to extends the original built Image)
  
  [Dockerfile.debug](https://github.com/geetHup9n0L/pwn_docker_setup/blob/main/Dockerfile.debug)

3. Build the debug image:
```c
docker build -t <pwn_dbg_challenge> -f Dockerfile.debug .
```
4. Run the debug container:
```c
docker run -it \
  --cap-add=SYS_PTRACE \
  --security-opt seccomp=unconfined \
  --name <pwn_dbg_container> \
  <pwn_dbg_challenge> \
  /bin/bash
```
* To return to container (in case you exited):
```c
docker start -ai babyshellcode_debug_container
```
* To delete container:
```c
docker rm -f <pwn_dbg_container>
```
**Notes:** change value `<name>` to your own preferred names
___
To initialize `gdb-pwndbg` debugging with python script

* First, enter:
```
tmux
```
* Then run the `exploit.py`
