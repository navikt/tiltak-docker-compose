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

## Start f eks opensearch
```
docker compose up opensearch
```

## Stop alt
```
docker compose down
```

## Volumer og lagring
Postgres-databasene lagrer i `/tmp/dbdata1`, `/tmp/dbdata2` og `/tmp/dbdata3`. For å slette data kan disse slettes før man starter det opp. Kafka og opensearch kjører pt uten lagring, altså kun "in memory". All data vil slettes ved omstart.
