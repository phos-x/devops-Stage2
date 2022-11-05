FROM python:3.7-alpine

WORKDIR /src

COPY requirements.txt /src

RUN apk update && \
apk add --no-cache --virtual build-deps gcc python3-dev musl-dev && \
apk add postgresql-dev

RUN pip install -r requirements.txt --no-cache-dir

COPY . /src
EXPOSE 8000

ENTRYPOINT ["python3"] 
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
