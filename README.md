# Example to publish a custom image to ghcr.io

Everything is in the [action script](https://github.com/tombrus/example-docker-image-publish/blob/main/.github/workflows/build.yaml), even the `Dockerfile`:-)

N.B. the action script needs a secret called `GHCR_TOKEN` with package read/write authorized token.

The first job:
- makes a docker image with
   - a simple `/hello_world.sh` script installed
   - the `jq` package/command, installed with `apt-get`
- then the docker image is uploaded to `ghcr.io`

The second job will use this image to:
- run the pre-installed `/hello_world.sh` script
- verify that `jq` is properly installed

I tried to keep the example as light as possible, just to show what you need to do to get this working.
