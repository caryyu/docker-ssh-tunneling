# docker-ssh-tunneling


## Environment Variables


### `SSH_USER=`

name of the user to connect via ssh


### `SSH_PASSWORD=`

password of the user to connect via ssh


## Run ssh-tunneling

```console
$ docker run -d --name ssh-tunneling -v /my/own/datadir:/ssh -p 2222:22 -e SSH_PERMITOPEN=mysql:3306 -e SSH_USER=user -e SSH_PASSWORD=secret --link some-mysql:mysql adito/ssh-tunneling
```

## Client (Linux and MacOS)

```shell
ssh -fNTRC rport:127.0.0.1:lport user@hostname -p ssh_port
```

## Reference

- https://ralf.ren/ssh-port-forward/

