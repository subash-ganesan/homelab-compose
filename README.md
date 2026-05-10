# Docker-compose

Compose files for our Homeden services

Bring up all the containers using below
`docker compose --profile "*" up -d`


## First time Git config setup

```
git config --global http."https://forgejo.homeden.com/".sslVerify false
git config --global user.email "homeden@homeden.com"
git config --global user.name "homeden"
```

## Encryption with SOPS & Age
```
age-keygen -o key.txt
export SOPS_AGE_KEY_FILE="key.txt"
find . -type f -name ".env" -exec sops -e -i {} \;
```

