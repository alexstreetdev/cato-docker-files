FROM alexstreet/opencv-base:3.4.4

RUN apt-get update && apt-get install -y \
 git

RUN git clone https://github.com/alexstreetdev/cato-detect

RUN pip3 install \
 argparse \
 jsonpickle \
 pika \
 requests \
 -i https://www.piwheels.hostedpi.com/simple

ENV rabbit_mq_host='127.0.0.1'
ENV username='vision'
ENV password='vision'

WORKDIR ./cato-detect

CMD python3 cato-detect.py -rh=${rabbit_mq_host} -un=${username} -pw=${password}

