FROM python:3

RUN mkdir -p /usr/src/poll/

WORKDIR /usr/src/poll

COPY requirements.txt /usr/src/poll/

RUN pip3 install -r /usr/src/poll/requirements.txt

COPY . /usr/src/poll/

EXPOSE 80

CMD [ "flask", "run", "--host=0.0.0.0", "--port=80" ]
