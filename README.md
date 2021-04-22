# git

[![Current Tag](https://img.shields.io/github/v/tag/dronehippie/git?sort=semver)](https://github.com/dronehippie/git) [![Build Status](http://drone.webhippie.de/api/badges/dronehippie/git/status.svg)](http://drone.webhippie.de/api/badges/dronehippie/git) [![Join the Matrix chat at https://matrix.to/#/#webhippie:matrix.org](https://img.shields.io/badge/matrix-%23webhippie-7bc9a4.svg)](https://matrix.to/#/#webhippie:matrix.org) [![Docker Size](https://img.shields.io/docker/image-size/dronehippie/git/latest)](https://hub.docker.com/r/dronehippie/git) [![Docker Pulls](https://img.shields.io/docker/pulls/dronehippie/git)](https://hub.docker.com/r/dronehippie/git) [![Go Reference](https://pkg.go.dev/badge/github.com/dronehippie/git.svg)](https://pkg.go.dev/github.com/dronehippie/git) [![Go Report Card](https://goreportcard.com/badge/github.com/dronehippie/git)](https://goreportcard.com/report/github.com/dronehippie/git) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/30d7a4b8a78947259d538e90879539d2)](https://www.codacy.com/gh/dronehippie/git/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dronehippie/git&amp;utm_campaign=Badge_Grade)

Drone plugin to handle Git operations. For the usage information and a listing of the available options please take a look at the [documentation](https://dronehippie.github.io/git/).

## Build

Build the binary with the following command:

```console
export GOOS=linux
export GOARCH=amd64

make build
```

## Docker

Build the image with the following command:

```console
docker build \
  --label org.opencontainers.image.source=https://github.com/dronehippie/git \
  --label org.opencontainers.image.revision=$(git rev-parse --short HEAD) \
  --label org.opencontainers.image.created=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
  --file docker/Dockerfile.amd64 --tag dronehippie/git .
```

## Usage

```console
docker run --rm \
  -e PLUGIN_DUMMY="dummy" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  dronehippie/git
```

## Security

If you find a security issue please contact [thomas@webhippie.de](mailto:thomas@webhippie.de) first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2021 Thomas Boerger <thomas@webhippie.de>
```
