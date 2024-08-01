# EvalJudge

## Prerequisites

- Make sure that Node.js (version>=16) is installed on your operating system.
- Make sure Docker is installed.

## Setup

Setup docker image:

- `cd docker`
- `./build`

Or

- `docker build -t evalengine .`

## Available Languages

Currently the supported languages are: `python2`, `python3`, `ruby`, and `javascript`

## Execute Endpoint

`POST http://localhost:3000/execute`
This endpoint requests execution of some arbitrary code.

```json
{
  "language": "node",
  "source": "console.log('testing')"
}
```

A typical response upon successful execution will contain `ran` and `output`.

```json
HTTP/1.1 200 OK
Content-Type: application/json

{
    "ran": true,
    "output": "testing\n"
}
```
