FROM debian:buster-slim

RUN apt-get update \
 && apt-cache depends texlive-full \
        | sed -rn 's/\W*Depends: //p' \
        | grep '^texlive-' \
        | grep -v -- '-doc$' \
        | grep -v '^texlive-fonts-extra' \
        | xargs apt-get install -y --no-install-recommends \
              make \
              latexmk \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN mkdir /document
WORKDIR /document

USER 1000:1000
