# docker-ssh-tunneling

A NAT-traversal solution by forwarding local port to a relay server, which can make NAT-behinded host could be accessed from the outside,

For example: Internet Host >> Local Host (Nat-behinded)

## Daemon Server

```console
$ docker run -d --name relay -p 2222:22 \
  -e SSH_USER=user -e SSH_PASSWORD=secret \
  <image>:<tag>
```

## Client (Linux and MacOS)

```shell
ssh -fNTRC rport:127.0.0.1:lport user@hostname -p ssh_port
```

## Reference

- https://ralf.ren/ssh-port-forward/

