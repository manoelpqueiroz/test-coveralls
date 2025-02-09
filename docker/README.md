# Docker for Python Project GH Coveralls

## Installation

To create a Docker image you can run:

```bash
invoke docker-build
```

This will create a default image `python-project-gh-coveralls:latest`.

You may provide multiple tags for the image, and you can also override the default `galactipy/python-project-gh-coveralls` repository:

```bash
invoke docker-build -t sometag
invoke docker-build -t latest -t sometag -r someuser/somerepo
```

## Usage

```bash
docker run -it --rm galactipy/python-project-gh-coveralls:latest
```

## How to clean up

To uninstall the default Docker image run:

```bash
invoke docker-remove
```

Again, you may also remove multiple tags:

```bash
invoke docker-remove -t latest -t sometag
```
