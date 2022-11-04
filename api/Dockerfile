FROM python:3.8.3-alpine

ENV dockerhome /home/app/django-app

RUN mkdir -p $dockerhome
WORKDIR $dockerhome

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
COPY . $dockerhome
RUN pip install -r requirements.txt
RUN python manage.py migrate

EXPOSE 8000

CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000" ]