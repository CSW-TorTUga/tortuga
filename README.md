# TorTUga

## Deployment

- Clone: `git clone --recurse-submodules https://github.com/CSW-TorTUga/tortuga.git`

- Build: `docker-compose build`
  
- Run: `docker-compose up -d`
  
- Stop: `docker-compose down`

- Import DB dump:

  ```
  echo "DROP DATABASE rms4csw; CREATE DATABASE rms4csw;" | docker exec -i tortuga_postgres_1 psql -U postgres
  cat dbdump/20211225_rms4csw_dump.sql | docker exec -i tortuga_postgres_1 psql -U postgres -d rms4csw
  ```
