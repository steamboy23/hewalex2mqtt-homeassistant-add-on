FROM python:3.7-alpine

RUN pip install -r pyserial configparser

// paho-mqtt

COPY  ./hewalex_geco/ ./hewagate/hewalex_geco/
COPY ./hewalex2mqttconfig.ini ./hewagate/hewalex2mqttconfig.ini
COPY ./*.py ./hewagate/

RUN ls -la /hewagate/*

ENTRYPOINT [ "python3", "/hewagate/hewalex2mqtt.py" ]
