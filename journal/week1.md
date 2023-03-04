# Week 1 — App Containerization

<<<<<<< HEAD
## Docerizing the backend app

`cd backend-flask`

create a Dockerfile and add the following codes
=======
## Containerize the BackEnd Application

```
cd backend-flask
```
create a Dockerfile and add the following code 
>>>>>>> 41a9423e370318924914289514426a0b964db2f5

```
FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt  requirements.txt
RUN pip3 install -r requirements.txt

COPY . .
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
<<<<<<< HEAD

```



=======
```
## Containerize Frontend

## Run NPM Install

We have to run NPM Install before building the container since it needs to copy the contents of node_modules

```
cd frontend-react-js
npm i
```


```
cd frontend-react-js
```
create another Dockerfile and add the follow code.

```
FROM node:16.18

ENV PORT=3000

COPY . /frontend-react-js
WORKDIR /frontend-react-js
RUN npm install
EXPOSE ${PORT}
CMD ["npm", "start"]
```
## Create a docker compose file  
Go back to  aws-bootcamp-cruddur-2023 directory
>>>>>>> 41a9423e370318924914289514426a0b964db2f5
