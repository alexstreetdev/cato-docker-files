FROM resin/raspberry-pi-python:2.7

WORKDIR app

RUN sudo apt-get update

RUN sudo apt-get install python-pip

RUN sudo pip install flask
RUN sudo pip install flask-restful

RUN git clone https://github.com/alexstreetdev/cato-camera-store

EXPOSE 5001

WORKDIR cato-camera-store

RUN ls

CMD python cato-camera-store.py
