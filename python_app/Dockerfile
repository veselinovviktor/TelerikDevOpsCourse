FROM ubuntu:22.04 AS basebuilder
COPY requirements.txt requirements.txt
RUN apt-get -yqq update; apt-get install -y python;apt-get install -y python3-pip;
RUN apt install -y python3.10-venv
RUN pip install -r requirements.txt

FROM basebuilder
COPY ./app .
CMD [ "python3", "app.py" ]
EXPOSE 5000