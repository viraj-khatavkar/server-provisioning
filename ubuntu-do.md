# server-provisioning

Add a new non-root user:

`sudo adduser viraj`

Add to the sudo user group:

`sudo usermode -a -G sudo viraj`

copy authorized ssh public keys from root user:

`cp ~/.ssh/authorized_keys /home/viraj/.ssh/authorized_keys`

Set the right ownership:

`chown -R viraj:viraj /home/viraj/.ssh/authorized_keys`
