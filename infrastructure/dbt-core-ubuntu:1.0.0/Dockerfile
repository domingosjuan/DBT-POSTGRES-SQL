FROM ubuntu:mantic

USER root

ADD ./requirements.txt /tmp/

RUN apt update -y
RUN apt install -y python3.11
RUN apt install -y python3.11-venv
RUN apt install -y python3-pip

RUN python3 -m venv dbt-env

RUN . dbt-env/bin/activate

RUN pip3 install --break-system-packages -r /tmp/requirements.txt

ENTRYPOINT ["/bin/bash"]