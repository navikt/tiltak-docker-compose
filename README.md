# tiltak-docker-compose
Oppset for å kjøre docker compose i Team Tiltak

## Start alt
```
docker compose up
``` 
eller
```
docker compose up -d
```
for å kjøre som daemons.

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
Postgres-databasene lagrer i `/tmp/dbdata-avtale`, `/tmp/dbdata-refusjon`, `/tmp/dbdata-okonomi` og `/tmp/dbdata-notifikasjon`. For å slette data kan disse slettes før man starter det opp. Kafka og opensearch kjører pt uten lagring, altså kun "in memory". All data vil slettes ved omstart.
