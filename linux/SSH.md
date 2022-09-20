## Setting up ssh
- create ssh key using ssh-keygen

```
    ssh-keygen -t ed25519 -C "myemail@eserv.net"
```
- copy id to remote machine

```
    ssh-copy-id <server-name@ip>
```

- verify on remote machine
```
    cat ~/.ssh/authorized_keys
```

- my need to add in client machine
```
    ssh-add <path to key>
```

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
### connect using specific key
```
    ssh -i ~/.ssh/mykey <username@ip> 
```


## References
- [Gitlab](https://docs.gitlab.com/ee/user/ssh.html)
- [Github](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
