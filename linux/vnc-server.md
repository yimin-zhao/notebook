## Install Tiger VNC

```
dnf groupinstall "Server with GUI"
dnf install tigervnc-server
```

Edit vnc user
```
vim /etc/tigervnc/vncserver.users
:2=username
```

Set a password for this TigerVNC server user
```
vncpasswd
```

Enable systemd daemon
```
systemctl enable --now vncserver@:2
```
Enter your server's public IP address and port 5902 as the VNC server.
