FROM python:3.7-alpine

RUN pip3 install paho-mqtt===1.5.0 pyserial configparser

ENTRYPOINT [ "python3", "/hewagate/hewalex2mqtt.py" ]
