# SSH Tunneling

It's a common practice to put your database in a private subnet, which means it is not accessible from outside of the network.

In order for Aidmin to communicate with a database that is not public, we support being able to communicate over a bastion host.

## Security Details

Aidmin generates a private key for your workspace (which is encrypted in our database and then again at rest) that it uses to communicate with your bastion host. Aidmin then expects a user called `aidmin` to be setup on the bastion host and provides a public key for passwordless authentication.

## Steps

1. Create a user called `aidmin` on the bastion host
   - Ubuntu: `sudo adduser aidmin --disabled-password`
   - Amazon Linux: `sudo adduser aidmin --password NP`
2. Login as root
   - `sudo su`
3. Create the authorized_keys file if it does not exist yet
   - `mkdir -p /home/aidmin/.ssh`
   - `touch /home/aidmin/.ssh/authorized_keys`
4. Use your favourite editor to add Aidmin's public key to the file
   - `vim /home/aidmin/.ssh/authorized_keys`
5. Set proper permissions on the authorized_keys file
   - `chmod 644 /home/aidmin/.ssh/authorized_keys`
   - `chown aidmin:aidmin /home/aidmin/.ssh/authorized_keys`
