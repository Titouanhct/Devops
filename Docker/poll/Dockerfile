FROM python:3
WORKDIR /app_py

COPY . /app_py

RUN pip3 install -r requirements.txt

EXPOSE 80

CMD flask run --host=0.0.0.0 --port=80
