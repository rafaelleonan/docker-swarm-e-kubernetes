FROM python:3.6
LABEL authors="rafaelleonan"

RUN apt-get update -y && apt-get install -y python3-pip python-dev

WORKDIR /app

RUN pip install Flask requests flask_mysqldb

COPY . .

EXPOSE 5000

CMD ["python", "./app.py"]