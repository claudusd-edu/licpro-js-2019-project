# LicPro Project 2019


## Structure
``` dir
README.md
back
  package.json
  src
front
  package.json
.gitingore
```

## API

This api should respect the lofic with http code status.

### List All

Request
```
GET /api/episodes
```

Response
``` json

[
  {
    "id": "A",
    "name": "The Big Bang Theory",
    "grade": 8,
    "code": "S01E01"
  },
  {
    "id": "B",
    "name": "The 100",
    "grade": 10,
    "code": "S01E01"
  }
]
```

### List One
Request
```
GET /api/episodes/B
```
Reponse
``` json
{
  "id": "B",
  "name": "The 100",
  "grade": 10,
  "code": "S01E01"
}
```

### Create en episode

Request
```
POST /api/episodes
```

``` json
{
  "name": "The 100",
  "grade": 10,
  "code": "S01E01"
}
```

Response
``` json
{"id": "C"}
```

### Delete an episode

Request
```
DELETE /api/episodes/C
```

### Update en episode

Request
```
PUT /api/episodes/A
```

``` json
{
  "name": "The 100",
  "grade": 10,
  "code": "S01E02"
}
```


## Storage V1

When i watch an episode i  make the HTTP Request ``POST /api/episodes/``. The system create a file in the dir ``back/data/``. The file name is ``{id}.json``.
