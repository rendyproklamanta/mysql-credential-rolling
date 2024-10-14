# Rolling user password credential

## Create dir and clone this repo to your server

```shell
mkdir -p /var/lib/mysql-credential-rolling
cd /var/lib/mysql-credential-rolling
git clone https://github.com/rendyproklamanta/docker-mysql-credential-rolling.git .
```

## Create docker secrets if not exist | if you have set before, just ignore it

```shell
nano secrets.sh
chmod +x secrets.sh && ./secrets.sh
```

## Need to change if you use mysql instead mariadb

```shell
nano users/rolling.sh

mariadb -u xxxxxx
mysql -u xxxxxx t
```

## Create Personal Access Token

- Go To gitlab setting
- Preference
- Access Tokens
- Checklist : api, read_api

## Edit yaml file

```shell
cd users
nano docker-compose.userxx.yaml
```

## Start the container

```shell
cd users
chmod +x start.sh && ./start.sh
```
