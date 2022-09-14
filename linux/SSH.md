start ssh agent in background

```
eval "$(ssh-agent -s)"
```

add ssh key

```
ssh-add ~/.ssh/nameofkey
```

### Generate ed25519 ssh key

```
    ssh-keygen -t ed25519 -C "myemail@eserv.net"
```
