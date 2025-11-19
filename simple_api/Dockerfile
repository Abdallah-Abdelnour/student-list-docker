FROM python:3.11-slim

LABEL maintainer="Abdelnour ABDALLAH <abdelnourabdallah@gmail.com>"

COPY requirements.txt /requirements.txt

RUN apt update -y && apt install -y python3-dev python3-pip libsasl2-dev libldap2-dev libssl-dev

RUN pip3 install -r /requirements.txt

COPY . /app

RUN mkdir /data

VOLUME ["/data"]

EXPOSE 5000

CMD ["python3", "/app/student_age.py"]