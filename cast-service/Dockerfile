FROM python:3.8-slim-buster

WORKDIR /app

COPY ./requirements.txt /app/requirements.txt

RUN apt-get update \
    && apt-get install gcc -y \
    && apt-get clean \
    && apt-get install libpq-dev -y

RUN pip install -r /app/requirements.txt \
    && rm -rf /root/.cache/pip

COPY . /app/