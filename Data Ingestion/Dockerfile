FROM python:3.9

#RUN pip list -> this was to know version of packkage wheel
RUN pip install pandas sqlalchemy fastparquet pyarrow psycopg2 psycopg psycopg2-binary psycopg-binary requests

# declare working directory
WORKDIR /app
COPY ingest_data.py ingest_data.py

#copy all files into current directory
COPY ingest_data.py ingest_data.py

#container will run in python mode and immediatly run pipeline.py
ENTRYPOINT [ "python", "ingest_data.py" ]