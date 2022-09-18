RUN pip3 install paho-mqtt pyserial configparser

COPY  ./hewalex_geco/ ./hewagate/hewalex_geco/
COPY ./hewalex2mqttconfig.ini ./hewagate/hewalex2mqttconfig.ini
COPY ./hewalex2mqtt.py ./hewagate/

RUN ls -la /hewagate/*

ENTRYPOINT [ "python3", "/hewagate/hewalex2mqtt.py" ]
