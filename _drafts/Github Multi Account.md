

In Wterminal or git bash,

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

```
ssh-keygen -t ed25519 -C "your_email@example.com" -f "path"
```

```
ssh-keygen -t ed25519 -C "your_email@example.com" -f "your_username"
```

```
ssh-add /path/to/your_key
```

```
ssh-add -l
```

```
git config --global core.sshCommand C:/Windows/System32/OpenSSH/ssh.exe
```