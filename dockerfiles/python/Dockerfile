FROM python:3.8.0

RUN apt-get update -y && \
    pip install --upgrade pip && \
    pip install poetry

WORKDIR /app

# 以下のRUNで必要なので
COPY pyproject.toml ./
COPY poetry.lock ./

RUN poetry config virtualenvs.create false
RUN poetry install

ENV TZ Asia/Tokyo

ENV DB_USER="user" \
    DB_PASSWORD="user"