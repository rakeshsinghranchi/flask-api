# flask-api

Here's a flask API. It's super simple and implements auth. Password is "stevie:wonder".

## Requirements

Get [cURL](https://curl.haxx.se/), and then get [Python](https://www.python.org/downloads/).

## Setup

Clone it:
```bash
$ git clone https://github.com/mkpt/flask-api.git
```
Create and activate a virtual environment:
```bash
$ virtualenv env
$ source env/bin/activate
```
Install dependencies and deactivate:
```bash
(env) $ pip install -r requirements.txt
(env) $ deactivate
```
Run it:
```bash
$ python app.py
```

## Usage

GET tasks
```
$ curl -i http://127.0.0.1:5000/todo/api/v1.0/tasks
```
GET task id 1
```
$ curl -i http://127.0.0.1:5000/todo/api/v1.0/tasks/1
```
CREATE task
```
$ curl -i -H "Content-Type: application/json" -X POST -d '{"title":"Read a book"}' http://127.0.0.1:5000/todo/api/v1.0/tasks
```
UPDATE task id 1
```
$ curl -i -H "Content-Type: application/json" -X PUT -d '{"title":"Need to find a good Python tutorial"}' http://127.0.0.1:5000/todo/api/v1.0/tasks/1
```
DELETE task id
```
$ curl http://127.0.0.1:5000/todo/api/v1.0/tasks/1 -X DELETE
```
