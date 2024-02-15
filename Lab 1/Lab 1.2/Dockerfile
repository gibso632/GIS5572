FROM python:3

WORKDIR /Lab 1/Lab 1.2

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "./app.py" ]
