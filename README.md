# tiltak-docker-compose
Oppset for å kjøre docker compose i Team Tiltak med kafka. 




## Start alt
```
docker-compose up --remove-orphans
``` 
eller
```
docker compose up -d
```
for å kjøre som daemons.

Starta tiltak-vedtaksbrev sin docker-compose (starter dokgen) og andre apper du vil ha flytet til


## Start en enkelt container
```
docker compose up opensearch
```
eller
```
docker compose up postgres-refusjon
```
## Stop alt
```
docker compose down
```

## Volumer og lagring
Postgres-databasene lagrer i 
```
volumes:
  dbdata-avtale:
  dbdata-refusjon:
  dbdata-okonomi:
  dbdata-notifikasjon:
  dbdata-vedtaksbrev:
```

For å slette data kan disse slettes før man starter det opp. Kafka og opensearch kjører pt uten lagring, altså kun "in memory". All data vil slettes ved omstart.


For å se hva som kan slettes
```
docker volume ls
```