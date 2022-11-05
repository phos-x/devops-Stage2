FROM python:3.7-alpine

WORKDIR /src

COPY requirements.txt /src

RUN pip install -r requirements.txt --no-cache-dir

COPY . /src
EXPOSE 8000

ENTRYPOINT ["python3"] 
CMD ["manage.py", "runserver", "0.0.0.0:8000"]