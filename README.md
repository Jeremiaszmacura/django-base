<hr />

## Development setup

<hr />

### Create python virutal enviroment

Create and active virtual enviroment using venv library:

```sh
python3 -m venv .venv
source .venv/bin/activate (Linux)
.venv\Scripts\activate (Windows)
```

In some Windows cases before activating venv:

```sh
Set-ExecutionPolicy Unrestricted -Scope Process
```

<hr />

### Run PosgreSQL database as container

```sh
docker run --name postgres_django -e POSTGRES_DB=dev_database -e POSTGRES_USER=dev_user -e POSTGRES_PASSWORD=dev_user -p 5432:5432 -d postgres:14
```

<hr />

### Run linter

Pytlint

```sh
python -m pylint <dir>
```

Black check

```sh
python -m black --check .
```

Black fix

```sh
python -m black .
```