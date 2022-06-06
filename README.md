
need to have mirror-registry.tar.gz in /output/mirror_registry

This was tested with a site.yaml

- name: test
  strategy: debug
  hosts: localhost
  remote_user: root
  vars:
  - quay_host_ip: 10.15.69.148
  - private_hostname: localhost
  - quay_hostname: localhost
  - json_pull_secret: /root/.docker/config.json
  - oc_mirror_tar_output: /root/mirror_seq1_000000.tar
  roles:
    - mirror-registry
