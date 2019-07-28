FROM python:3.6.0-alpine

WORKDIR /app
ADD . /app

RUN apk add --no-cache --virtual gcc 
RUN apk add --no-cache --virtual libc-dev
#RUN pip install --upgrade pip
RUN pip install -r /app/requirements.txt

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

CMD ["python3", "post_app.py"]