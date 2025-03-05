Create certificate
1. make directory in host
mkdir /opt/snipeit/ssl/
convert snipeit.crt to snipe.csr
then paste to Certificate server the snipeit.cer 
the select certiciate template web server + key
add attribute
san:dns=[hostname].[domain]&[hostname].[domain]
then submit
download der certificate for windows and base64 for linux
then copy and paste the snipeit.cer
to the host machine
then create an nginx file to map the ssl

Configure Snipeit
1. in snipe it docker compose file make sure that 
port is 443
the ssl is map to the  docker make sure the name is snipeit-ssl.cer as documented in snipeit docs
https://snipe-it.readme.io/docs/docker#ssl-enabled

example
- /opt/snipeit/ssl/snipeit.cer:/var/lib/snipeit/ssl/snipeit-ssl.crt:ro
      - /opt/snipeit/ssl/snipeit.key:/var/lib/snipeit/ssl/snipeit-ssl.key:ro


note: you cannot go trough pre-flight if you don't have ssl in the snipe it
https://snipe-it.readme.io/docs/docker#ssl-enabled

