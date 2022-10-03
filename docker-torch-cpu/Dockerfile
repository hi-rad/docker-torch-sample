FROM python:3.9
ADD . /code
WORKDIR /code
COPY requirements.txt requirements.txt
RUN pip -q install pip --upgrade
RUN pip install -r requirements.txt