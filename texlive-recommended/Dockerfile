FROM debian:buster-slim

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
        texlive-latex-base \
        texlive-latex-recommended \
        texlive-latex-extra \
        texlive-font-utils \
        texlive-fonts-recommended \
        texlive-lang-portuguese \
        texlive-plain-generic \
        texlive-publishers \
        texlive-science \
        ghostscript \
        make \
        latexmk \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN mkdir /document
WORKDIR /document

USER 1000:1000
