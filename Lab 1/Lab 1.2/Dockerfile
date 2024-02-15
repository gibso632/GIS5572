FROM python:3.10-slim

WORKDIR Lab 1/Lab 1.2/app

COPY . /app

RUN pip install --trusted-host pypi.python.org -r requirements.txt

EXPOSE 8080

ENV NAME World

CMD ["python","app.py"]
