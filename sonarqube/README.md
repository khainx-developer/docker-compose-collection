# Sonarqube

## Increase Linux setting https://docs.sonarqube.org/latest/requirements/requirements/#header-5

```
sudo sysctl -w vm.max_map_count=524288
sudo sysctl -w fs.file-max=131072
```

## Increase Windows WSL setting

```
wsl -d docker-desktop
sysctl -w vm.max_map_count=524288
sysctl -w fs.file-max=131072
```

## Start Sonarqube on localhost

Persisting your database

```
sudo mkdir -p ./database/sonardb
sudo chown -R 1001:1001 ./database/sonardb
```

## Run command to start service

```
docker-compose -f docker-compose.yml up -d
```

Open `http://localhost:9000` and login by username `admin`, password `admin`

## Create token

Open http://localhost:9000/account/security/ then generate a token
