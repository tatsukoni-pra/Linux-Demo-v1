FROM debian:bookworm

RUN apt-get update && apt-get install -y --no-install-recommends \
  build-essential \
  man-db \
  dumb-init

WORKDIR /app
COPY . /app
RUN chmod 777 /app/docker/entrypoint.sh

ENTRYPOINT [ "dumb-init", "sh", "/app/docker/entrypoint.sh" ]
