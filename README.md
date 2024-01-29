# ZoomCamp2024

======================================================================================
======================================================================================
# 1. this for run docker-compose.yaml file to up Postgres DB & pgAdmin together in the same network
docker compose up

# 2. build the image to dockerize ingest_data.py 
docker build -t green_taxi_final5

"""
run container of image green_taxi_final5 giving:
- homework_default, which is network name where postgres DB & pgAdmin built
(run docker network ls, to find all docker networks & choose one which name has directory name where you build docker-compose file)
- postgrersDB, hostname will find as service name in docker-compose.yaml file which build postgres DB
- other arguments also needed to connect & ingest data to postgres DB
"""
docker run -it --network=zoomcamp2024_default green_taxi_final5:latest --user=root --password=root --host=postgrersDB --port=5432 --db=ny_taxi --taxi_table_name=green_taxi_data  --zones_table_name=zones
======================================================================================
======================================================================================