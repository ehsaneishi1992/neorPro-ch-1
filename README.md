# neorPro-ch-1
ssh to other nodes with private key 
```bash
nano ~/.ssh/config
```
```sshconfig
Host bastion
    HostName 188.121.117.192
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem

Host ch1-master-1
    HostName 172.16.0.152
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem
    ProxyJump bastion

Host ch1-master-2
    HostName 172.16.0.207
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem
    ProxyJump bastion

Host ch1-master-3
    HostName 172.16.0.24
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem
    ProxyJump bastion

Host ch1-worker-1
    HostName 172.16.0.88
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem
    ProxyJump bastion

Host ch1-worker-2
    HostName 172.16.0.224
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem
    ProxyJump bastion

Host ch1-worker-3
    HostName 172.16.0.172
    User ubuntu
    IdentityFile ~/.ssh/ch1.pem
    ProxyJump bastion
```
