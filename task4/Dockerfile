FROM ubuntu:16.04

# Install python flask depedency
RUN apt-get update -y && \
    apt-get install -y python-pip python-dev

# Copy requirements.txt from local workspace
COPY ./task4/requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip install -r requirements.txt

# Copy source code from local workspace
COPY ./task4/mockAPI.py /app/mockAPI.py

ENTRYPOINT [ "python" ]

CMD [ "mockAPI.py" ]