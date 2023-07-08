FROM python:3.8-slim
RUN apt update -y && \
    pip install pip --upgrade

WORKDIR /app/

ADD requirements.txt .

RUN pip install -r requirements.txt

COPY . .

ENTRYPOINT [ "uvicorn", "app:app", "--host", "0.0.0.0"]