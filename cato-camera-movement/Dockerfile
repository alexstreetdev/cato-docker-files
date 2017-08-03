FROM alexstreet/opencv-base

RUN sudo apt-get update

RUN sudo apt-get install python-pip

RUN pip install imutils

WORKDIR app

RUN git clone https://github.com/alexstreetdev/cato-camera-movement

ENV input_url=''
ENV output_url=''
ENV camera_name='camera'
ENV threshold=10000

CMD python ./cato-camera-movement/cato-camera-movement.py -i ${input_url} -o ${output_url} -n ${camera_name} -t ${threshold}
