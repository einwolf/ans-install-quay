# Install services

Install project quay

```bash
# Test ping
ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook -v ping.yaml -l repo1

# Test generate the service unit files
QUADLET_UNIT_DIRS=$(pwd)/roles/install-quay_quad/files/etc/containers/systemd/ /usr/lib/systemd/system-generators/podman-system-generator --dryrun
```

```bash
# podman multip pod version
ansible-playbook -v install-quay_quad_pod.yaml -l repo1

# podman play kube version
ansible-playbook -v install-quay_quad_kube.yaml -l repo1
```

