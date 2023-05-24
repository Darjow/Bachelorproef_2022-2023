FROM debian:bullseye

RUN apt update && apt-get install -y \
    texlive-latex-base \
    texlive-latex-extra \
    texlive-lang-european \
    texlive-bibtex-extra \
    biber \
    git \
    texstudio \
    jabref \
    r-base \
    texlive-xetex \
    python3-pip \
    latexmk \
    && pip install pygments \
    && rm -rf /var/lib/apt/lists/*

RUN tlmgr update --self && tlmgr install dramatist

COPY fonts/ /usr/share/fonts/opentype
RUN fc-cache -f -v
