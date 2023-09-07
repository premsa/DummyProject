# README

This repository describes my ordinary workflow for implementing small python-based projects with docker and poetry. You only need docker pre-instlled on your system. 

#### Build the docker development image:
```
docker build -f development.Dockerfile -t development .
```

#### Run the docker container:
```
docker run -it development
```

#### In the container initialize the pyproject.toml for an empty project interactively with:
```
poetry init
```

#### Alternatively, libraries may be added afterwards with:

```
poetry add 
```

#### From the project with a (pre-existing) pyproject.toml, we install our dependencies into a virtual environment


```
poetry config virtualenvs.in-project true

poetry install
```

#### Finally, we access our virtual enviroment in a shell with:

```
poetry shell
(shell) ls
(shell) python -m application.main
```

#### or, we run the command directly

```
poetry run python -m application.main
```
