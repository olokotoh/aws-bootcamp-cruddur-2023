# Week 1 — App Containerization

## Docerizing the backend app

`cd backend-flask`

create a Dockerfile and add the following codes

```
FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt  requirements.txt
RUN pip3 install -r requirements.txt

COPY . .
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

```



