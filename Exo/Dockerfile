FROM ubuntu:plucky

WORKDIR /srv/app

RUN apt -y update && \
    apt install -y python3.12-venv python3-pip git && \
    git clone https://github.com/exo-explore/exo.git && \
    python3 -m pip config set global.break-system-packages true && \
    cd /srv/app/exo && \
    pip install -e . && \
    pip install opencv-python-headless==4.11.0.86

EXPOSE 52415

ENTRYPOINT /srv/app/exo/bin/exo