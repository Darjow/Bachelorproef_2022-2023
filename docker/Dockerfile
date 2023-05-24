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
    && apt-get install -y texlive-generic-extra

RUN apt-get install -y texlive-science texlive-publishers texlive-humanities texlive-latex-recommended texlive-fonts-extra

RUN tlmgr update --self && tlmgr install dramatist

COPY fonts/ /usr/share/fonts/opentype
RUN fc-cache -f -v
