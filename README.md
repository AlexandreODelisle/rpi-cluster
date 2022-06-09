# BootStrap a K3S Cluster using `k3sup` and `ansible` on a RPI cluster

## Notes

k3sup needs to use at least a ecdsa cryptographic key to be able to `ssh` into the remote hosts.

```shell
sh-keygen -t ecdsa
ssh-copy-id -i ~/.ssh/id_ecdsa $SERVER_USER@$SERVER_IP

```

## Need to define docker login creds prior

```shell

docker login

# if permission denied
sudo usermod -aG docker $USER

```

## Inspiration

k3s bootstrap inspiration:
- https://github.com/loeken/bootstrap-k3s