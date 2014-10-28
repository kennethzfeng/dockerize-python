FROM kennethzfeng/dockerize-python:3.4.1

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY . /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install -r requirements.txt

ONBUILD COPY bower.json /usr/src/app/
ONBUILD RUN bower install --allow-root
