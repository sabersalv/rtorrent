# RTorrent BitTorrent Client

> [Original README](./README.original.md) [jesec/rtorrent](https://github.com/jesec/rtorrent) [Vanilla rTorrent](https://github.com/rakshasa/rtorrent)

- [Sequential download](https://github.com/jesec/rtorrent/commit/bd904e366367cb9cbe007381089eea066253c9e9)
- XML RPC -> JSON RPC

At the moment, build failed with [std::binary_function' is deprecated](https://github.com/jesec/rtorrent/issues/54)

## Build

```sh
brew install bazel
bazel build rtorrent
# Binary available at bazel-bin/rtorrent

# Build with docker
docker build .
docker buildx build --platform linux/amd64 .   
```

## Release

```sh
git tag v0.9.8-1
git push --tags
# Github Actions will build and publish to Docker Hub
```