# apache2-enable-https-SSL
`enable ssl via (apache2) https debian

apt install python-certbot-apache 


# replace <domain> with current sitename via DNS registration 
sudo certbot --authenticator standalone --installer apache \
  -d <domain> --pre-hook "service apache2 stop" --post-hook "service apache2 start"
