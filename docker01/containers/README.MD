## Start All Container
```bash
docker-compose ()
{
    docker-compose $(find -name 'docker-compose*.yml' -type f -printf '%p\t%d\n'  2>/dev/null | sort -n -k2 | cut -f 1 | awk '{print "-f "$0}') $@
}
```


## Start Single Container

You need to link the .env file from the Containerfolder:
```
ln ../.env .env
```

Then start the docker-compose
```
docker-compose -f docker-compose*.yml up -d
```
