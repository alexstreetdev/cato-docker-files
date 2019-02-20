FROM resin/rpi-raspbian:stretch

# see https://blog.piwheels.org/new-opencv-builds/
# for dependencies 

RUN apt-get update && apt-get install -y \
 pkg-config \
 python3 \
 wget \
 libatlas3-base \
 libwebp6 \
 libqt4-test \
 libtiff5 \
 libjasper1 \
 libilmbase12 \
 libopenexr22 \
 libgstreamer1.0-0 \
 libavcodec57 \
 libavformat57 \
 libavutil55 \
 libswscale4 \
 libqtgui4 \
 libqtcore4

RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python3 get-pip.py
RUN pip3 install numpy -i https://www.piwheels.hostedpi.com/simple

RUN pip3 install opencv-python -i https://www.piwheels.hostedpi.com/simple

