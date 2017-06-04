# install-nextcloud-collabora

## Local install

I installed nextcloud12 using collabora repositories for Debian 8 as explained in [collaboraoffice's doc](https://www.collaboraoffice.com/code/#getting_set_up)

I configured apache2 to use ssl 

See [/etc/apache2/sites-enabled/default-ssl.conf](https://github.com/makayabou/install-nextcloud-collabora/blob/master/default-ssl.conf)

See [/etc/apache2/sites-enabled/nextcloud.conf](https://github.com/makayabou/install-nextcloud-collabora/blob/master/nextcloud.conf)


I can't access to http://localhost/nextcloud    but I can access https://localhost/nextcloud, so it seems that I configured nextcloud with SSL . I'm not very sure it's well done, I don't really understand how ssl works.

I created my autosigned certificat using: 
```bash
sudo openssl req -new -x509 -days 365 -nodes -out /etc/ssl/localcerts/apache.pem -keyout /etc/ssl/localcerts/apache.key
```

and my answers were:
```
Country Name (2 letter code) [AU]:FR
State or Province Name (full name) [Some-State]:France
Locality Name (eg, city) []:Paris
Organization Name (eg, company) [Internet Widgits Pty Ltd]:
Organizational Unit Name (eg, section) []:
Common Name (e.g. server FQDN or YOUR name) []:localhost
Email Address []:
```

but when I want to indicate Nextcloud Collabora's addresss, it popsup  *Saved with error: Collabora Online should use the same protocol as the server installation. *

See [/etc/apache2/sites-enabled/collabora.conf](https://github.com/makayabou/install-nextcloud-collabora/blob/master/collabora.conf)

See [/etc/apache2/sites-enabled/collabora-ssl.conf](https://github.com/makayabou/install-nextcloud-collabora/blob/master/collabora-ssl.conf)
