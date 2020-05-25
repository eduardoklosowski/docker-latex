FROM debian:buster-slim

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
        texlive-full \
        make \
        latexmk \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN mkdir /document
WORKDIR /document

USER 1000:1000
