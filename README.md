# OpenVPN-Free-Panel
BytesPH Official Free Panel Instruction

To install: 
```
wget -N --no-check-certificate -q -O installer https://gitfront.io/r/user-1492265/3vNGy9UvfShc/OpenVPN-Installer/raw/FreePanel && chmod +x installer && ./installer
```

On your server.conf file paste these lines
```
client-connect /etc/openvpn/login/connect.sh
client-disconnect /etc/openvpn/login/disconnect.sh
auth-user-pass-verify "/etc/openvpn/login/auth_vpn" via-env
```

Then restart OpenVPN service
```
service openvpn restart
```
