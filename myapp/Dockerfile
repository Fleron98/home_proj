FROM ubuntu:24.04
WORKDIR /myapp

RUN apt-get update && apt-get install -y 

COPY requirements.txt requirements.txt
COPY . /myapp
ENV FLASK_APP=app
EXPOSE 5000
CMD ["/myapp/venv/bin/flask", "run", "--host=0.0.0.0"]
