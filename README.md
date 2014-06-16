mhn_postgres
=================

PostgreSQL for Docker. The data directory is set to `/data` so you can use a data only volume.

    $ docker run -name postgresql-data -v /data ubuntu /bin/bash
    $ docker run -d -p 5432:5432 -volumes-from postgresql-data -e POSTGRESQL_USER=ssc -e POSTGRESQL_PASS=trustno1 -e POSTGRESQL_DB=devpg smlbenu/mhn_postgresk
    
    $ psql -h localhost -U ssc devpg
    Password for user :
    trustno1
    Type "help" for help.

    docker=#

(Example assumes PostgreSQL client is installed on Docker host.)

