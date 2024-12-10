# OpenStack provider for DevPod

This is a machine provider that creates machines on OpenStack using the `openstack` CLI directly.
You will need to install the `openstack` CLI in order to use this provider.

Example usage:

```bash
devpod provider add ./provider.yaml --option OS_CLOUD=my-cloud --option NETWORK=abc-def-123 \
  --option KEY_PAIR=my-key-pair --option FLAVOR=m1.medium --option IMAGE=ubuntu-24.04 \
  --option JUMPHOST=my-jumphost --option SSH_USER=ubuntu --option VOLUME=100
devpod machine create demo-devpod --provider=openstack
devpod machine ssh demo-devpod
```
