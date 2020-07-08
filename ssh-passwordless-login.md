# SSH and Passwordless login

## Generating keypairs

Move into the ~/.ssh/ directory in your user home.

```
cd ~/.ssh/
```

Then generate a new keypair through the ssh-keygen command.

```
ssh-keygen -t rsa -b 4096 -C "EMAIL-OR-NICKNAME"
```

You will be prompted to choose a KEYNAME and a passphrase for your keypair.

This command will create two new keys into the current directory.

- (*private key*) KEYNAME
- (*public key*) KEYNAME.pub

## Copying the public key to the server

To copy your public key inside the USERNAME's ~/.ssh/authorized_keys file.

```
ssh-copy-id -i ~/.ssh/KEYNAME.pub USERNAME@SERVER-IP-ADDRESS
```

Enjoy!
