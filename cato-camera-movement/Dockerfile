FROM alexstreet/opencv-base

RUN sudo apt-get update

RUN sudo apt-get install python-pip

RUN pip install imutils

WORKDIR app

RUN git clone https://github.com/alexstreetdev/cato-camera-movement

CMD ["python", "./cato-camera-movement/cato-camera-movement.py"]
