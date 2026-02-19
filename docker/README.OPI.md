After following the instructions in the LOCAL\_DEV.md file, do the following to build and push the images:

`task build:all REGISTRY=ghcr.io IMAGE_OWNER=balt-opi VERSION=v1.0.0 PLATFORMS="linux/amd64"`
`podman push ghcr.io/balt-opi/pgduck-server:v1.0.0-pg18; podman push ghcr.io/balt-opi/pgduck-server:v1.0.0-pg18-almalinux; podman push ghcr.io/balt-opi/pg_lake:v1.0.0-pg18; podman push ghcr.io/balt-opi/pg_lake:v1.0.0-pg18-almalinux;`

After you have the compose project running in sudo-land, execute the following to make the test bucket:
`sudo podman exec -it localstack-main bash -c "/init-s3.sh"`
