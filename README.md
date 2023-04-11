# Introduction

Install and run an GLPI and phpmyadmin instance with docker 

## Default accounts

More info in the 📄[Docs](https://glpi-install.readthedocs.io/en/latest/install/wizard.html#end-of-installation)

| Login/Password     	| Role              	|
|--------------------	|-------------------	|
| glpi/glpi          	| admin account     	|
| tech/tech          	| technical account 	|
| normal/normal      	| "normal" account  	|
| post-only/postonly 	| post-only account 	|


## Deploy with persistence data

volumes:
  data_db:
  data_glpi:

To deploy with docker compose, you use *docker-compose.yml* and *mariadb.env* file.
You can modify **_mariadb.env_** to personalize settings like :

* MariaDB root password
* GLPI database
* GLPI user database
* GLPI user password


### mariadb.env
```
MARIADB_ROOT_PASSWORD=lthat
MARIADB_DATABASE=glpidb
MARIADB_USER=glpi_user
MARIADB_PASSWORD=glpi
```


To deploy, just run the following command on the same directory as files

```sh
docker-compose up -d
```

# Environnment variables

## TIMEZONE

TIMEZONE=Europe/Paris

