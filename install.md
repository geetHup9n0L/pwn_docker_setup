### Docker Installation on Kali:

* Install Docker and the container tools:
```c
sudo apt update
sudo apt install -y docker.io
```

* Start and Enable the Docker Service:
```c
sudo systemctl enable --now docker
```

* Add your user to the Docker group:
```c
sudo usermod -aG docker $USER
```

* Reboot the machine

___ 
More documentation at: https://www.kali.org/docs/containers/installing-docker-on-kali/
