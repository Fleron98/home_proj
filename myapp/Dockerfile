FROM ubuntu:24.04
WORKDIR /myapp

RUN apt-get update && apt-get install -y python3 python3-pip python3-venv

COPY requirements.txt requirements.txt
RUN python3 -m venv /myapp/venv 
RUN /myapp/venv/bin/pip install -r requirements.txt
COPY . /myapp
ENV FLASK_APP=app
EXPOSE 5000
CMD ["/myapp/venv/bin/flask", "run", "--host=0.0.0.0"]
