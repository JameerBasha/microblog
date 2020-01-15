FROM docker.io/python:3.7

WORKDIR /app

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

RUN pip install gunicorn

EXPOSE 8000

COPY . . 

CMD ["/usr/local/bin/gunicorn","-b","0.0.0.0:8000","wsgi:app"]
