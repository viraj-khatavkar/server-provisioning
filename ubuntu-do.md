# server-provisioning

```
# Add a new non-root user:
sudo adduser viraj

# Add to the sudo user group:
sudo usermod -a -G sudo viraj

# copy authorized ssh public keys from root user:
cp ~/.ssh/authorized_keys /home/viraj/.ssh/authorized_keys

#Set the proper ownership:
chown -R viraj:viraj /home/viraj/.ssh/authorized_keys
```

Firewall:

```bash
sudo ufw status verbose

sudo ufw default deny incoming
sudo ufw default allow outgoing

sudo ufw allow ssh
sudo ufw allow http
sudo ufw allow https
sudo ufw limit ssh

sudo ufw enable

```
