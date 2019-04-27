FROM python:2.7.15-alpine3.8
#FROM python:2.7.15-stretch

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY paho.mqtt.python ./paho.mqtt.python
RUN cd paho.mqtt.python && ls && pwd && python setup.py install

COPY . .

CMD [ "python", "./mqtt_db_plugin.py" ]
