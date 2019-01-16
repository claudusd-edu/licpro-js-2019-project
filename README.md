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

```
GET /api/episodes

[
  {
    "id": "A"
    "name": "The Big Bang Theory",
    "grade": 8,
    "code": "S01E01"
  },
  {
    "id": "B"
    "name": "The 100",
    "grade": 10,
    "code": "S01E01"
  }
]
```

```
GET /api/episodes/B

{
  "id": "A"
  "name": "The 100",
  "grade": 10,
  "code": "S01E01"
}
```

```
POST /api/episodes
{
  "id": "A"
  "name": "The 100",
  "grade": 10,
  "code": "S01E01"
}

{"id": "C"}
```

## Storage V1

When i watch an episode i  make the HTTP Request ``POST /api/episodes/``. The system create a file in the dir ``back/data/``. The file name is ``{id}.json``.
