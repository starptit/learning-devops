###########
# BUILDER #
###########

FROM python:3.8-buster as builder

ARG DEBIAN_FRONTEND=noninteractive


RUN mkdir /logs
ENV LOG_DIR /logs

WORKDIR /app

COPY requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

COPY . /app

EXPOSE 8000

ENV PYTHONUNBUFFERED 1
