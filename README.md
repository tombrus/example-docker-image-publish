# Example to publish a custom image to ghcr.io

What the first job does:
- a docker image is constructed with
- - a simple `/hello_world.sh` script installed
- - the `jq` package/command is installed with `apt-get`
- then the docker image is uploaded to `ghcr.io`

The second job will ise this image to run on:
- run the pre-installed `/hello_world.sh` script
- verify that `jq` is properly installed

Everything is in the github action script, even the `Dockerfile`:-)
