# Terraform provider for libvirt (macOS build)

This repo is entirely based on [Duncan's repo](https://github.com/dmacvicar/terraform-provider-libvirt) and simply provides an additional pre-built bin for darwin-based architectures.

## Installation

You can simply grab the pre-built bin from the [Releases tab](https://github.com/thundersquared/terraform-provider-libvirt/releases) and place it under your Terraform plugins directory. Here's an alternative illustrating how to do it programmatically and possibly getting the latest version too:

```shell script
mkdir -p  ~/.terraform.d/plugins/
LIBVIRT_PROVIDER_VERSION=$(curl -s https://api.github.com/repos/thundersquared/terraform-provider-libvirt/releases/latest | grep 'tag_name' | cut -d\" -f4)
curl -L "https://github.com/thundersquared/terraform-provider-libvirt/releases/download/${LIBVIRT_PROVIDER_VERSION}/terraform-provider-libvirt" -o ~/.terraform.d/plugins/terraform-provider-libvirt
```

## License

Inheriting Apache License 2.0, which you can have a look at [source repo](https://github.com/dmacvicar/terraform-provider-libvirt/blob/master/LICENSE).
