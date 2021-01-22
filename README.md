# squid-proxy-installer

Auto install Squid 3 proxy on

* Ubuntu 20.04
* Ubuntu 18.04
* Ubuntu 16.04
* Ubuntu 14.04
* Debian 10
* Debian 9
* Debian 8


## Install Squid

To install, run the script

```
wget https://raw.githubusercontent.com/serverok/squid-proxy-installer/master/squid3-install.sh
sudo bash squid3-install.sh
```

# Configure Multiple IP Address

NOTE: This is only needed if you have more than one IP on your server.

Before you can configure squid to use muliple IP address, you need to add IP to your server and you should be able to connect to server using these IPs.

Once IP added to your server, you can configure it to use with squid proxy by running following command

```
wget https://raw.githubusercontent.com/serverok/squid-proxy-installer/master/squid-conf-ip.sh
sudo bash squid-conf-ip.sh
```

# Create Users

To create users, run

```
sudo /usr/bin/htpasswd -b -c /etc/squid/passwd USERNAME_HERE PASSWORD_HERE
```

To update password for am existing user, run

```
sudo /usr/bin/htpasswd /etc/squid/passwd USERNAME_HERE
```

replace USERNAME_HERE and PASSWORD_HERE with your desired user name and password.

Restart squid proxy

```
sudo systemctl restart squid
```

# Support

If you are looking for paid support, contact me

https://serverok.in/contact
