####
#### WARNING: Please DO NOT chek in any sensitive information in local.cfg or local.cfg.template
#### This is Kazoo-Configs-Kamailio for Kamailio 5.8
####

#####
##### (1) The following lines in the `local.cfg` file must be updated for Kamailio to function properly.
#####

````
#!substdef "!MY_HOSTNAME!kamailio.2600hz.com!g"
#!substdef "!MY_IP_ADDRESS!127.0.0.1!g"
#!substdef "!MY_IP_ADDRESS_EXTERNAL!127.0.0.1!g"
#!substdef "!MY_AMQP_URL!amqp://guest:guest@127.0.0.1:5672!g"
#!substdef "!KAZOO_DB_URL!postgres://kamailio:kamailio@127.0.0.1/kamailio!g"
```
####
#### (2) Or use `envsubst` replace envvars in `local.cfg.templace` to generate `local.cfg` 
#### e.g. export MY_HOSTNAME=my.host.io; export ...; envsubst < local.cfg.template > local.cfg
####

```
#!substdef "!MY_HOSTNAME!${MY_HOSTNAME}!g"
#!substdef "!MY_IP_ADDRESS!${MY_IP_ADDRESS}!g"
#!substdef "!MY_IP_ADDRESS_EXTERNAL!${MY_IP_ADDRESS_EXTERNAL}!g"
#!substdef "!MY_AMQP_URL!amqp://${MY_AMQP_USER}:${MY_AMQP_PASSWORD}@${MY_AMQP_HOST}:${MY_AMQP_PORT}!g"
#!substdef "!KAZOO_DB_URL!postgres://${KAZOO_DB_USER}:${KAZOO_DB_PASSWORD}@${KAZOO_DB_HOST}/${KAZOO_DB_NAME}!g"
```

#
# (3) Copy TLS certificste and key to tls/kamailio.pem
#
