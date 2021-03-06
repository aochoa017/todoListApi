# todoListApi
In this repository I want to show you how to implement an easy **RESTful API** in **Node.js**.

## Installation
```bash
git clone https://github.com/aochoa017/todoListApi.git
```
## Usage
```bash
$ npm init
```
```bash
$ npm run start
```
RESTful API is now running in your localhost at port 3000.

There are 2 endpoints in this demo: `/tasks` and `/tasks/:taskId`

| Endpoint      | Method        | Description  |
| ------------- | ------------- | ----- |
| /tasks      | GET | Get all post item registers |
| /tasks      | POST      | Create new item  |

## Examples

### Curl

```bash
curl -X GET \ http://localhost:3000/tasks
```

```bash
curl -X POST \ http://localhost:3000/tasks \ -H 'content-type: application/x-www-form-urlencoded' \ -d name=Read%20nodejs%20server%20in%2010%20minutes
```

### Ajax
```bash
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "http://localhost:3000/tasks",
  "method": "GET",
  "headers": {}
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```bash
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "http://localhost:3000/tasks",
  "method": "POST",
  "headers": {
    "content-type": "application/x-www-form-urlencoded"
  },
  "data": {
    "name": "Read nodejs server in 10 minutes"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

\* If you need other language examples ask me to put them in README.md

## Acknowledgements

[Build Node.js RESTful APIs in 10 Minutes](https://www.codementor.io/olatundegaruba/nodejs-restful-apis-in-10-minutes-q0sgsfhbd)
