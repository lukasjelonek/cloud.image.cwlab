# Recipe for a image running cwlab

Image that downloads and starts a cwlab container with docker on startup of the vm.

## Development

This cloud image is based on [diskimage-builder](https://docs.openstack.org/diskimage-builder/latest/) 
and [dib-builder](https://github.com/ag-computational-bio/dib-builder). `dib-builder` is a small script
collection to build and upload `diskimage-builder` images.

### Content

* `config.yaml` - Configuration file for `dib-builder`
* `elements/` - Elements for `diskimage-builder`
* `elements/docker/` - Installs docker in the image and adds the system user to the docker group
* `elements/cwlab/` - Adds script to the image that starts cwlab on start of a vm

### Build image

```
dibt-build
```

### Deploy image to a openstack cloud

```
source <your-cloud-project-openrc>
dibt-deploy
```

