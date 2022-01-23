FROM python:3.10.2-alpine3.15

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

CMD [ "python", "./helloworld.py" ]
