# Ubuntu Server First Login

## Logging as root

First of all login as root.

```
ssh root@SERVER-IP-ADDRESS
```

## Create a substitute user for root

Create another user that will be as powerful as root, without being root.

```
sudo adduser USERNAME
sudo usermod -a -G adm USERNAME
sudo usermod -a -G sudo USERNAME
```

## Lock root access

Make sure that logging in as root with a password is impossible.

(Before running the following command, make sure that you can login as USERNAME)

```
sudo usermod -p "!" root
```

Now you can login as USERNAME and use sudo when necessary.

```
ssh USERNAME@SERVER-IP-ADDRESS
```

Enjoy!
