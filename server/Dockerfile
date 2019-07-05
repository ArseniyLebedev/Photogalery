FROM python:3.7.3
RUN apt-get update

RUN mkdir -p /app/user/static
RUN mkdir /src
WORKDIR /app
ADD requirements.txt /app
RUN pip install --upgrade pip
RUN pip install --src /src -r requirements.txt
ADD . /app
RUN python ./manage.py collectstatic --noinput
EXPOSE 8000