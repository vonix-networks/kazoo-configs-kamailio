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

#####
##### (2) Copy TLS certificste and key to tls/kamailio.pem
#####
