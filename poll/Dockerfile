FROM python:3

ADD . /app

WORKDIR /app

RUN pip3 install -r requirements.txt

COPY . /app

EXPOSE 80

CMD flask run --host=0.0.0.0 --port=80