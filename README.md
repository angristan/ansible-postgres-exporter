# Ansible role for Postgres exporter

This role will setup [postgres_exporter](https://github.com/prometheus-community/postgres_exporter) on any Linux machine using systemd.

## Role Variables

- `postgres_exporter_version`: the version of Postgres exporter that will be installed.

The role will download the Postgres exporter release on the deployer and upload the binary to the target host.

If the `/usr/local/bin/postgres_exporter` binary already exists, the role will skip the install steps. You can force them (to update, for instance), by setting `postgres_exporter_force_install` to true.

- `postgres_exporter_web_listen_address`: the address Node exporter will listen on. (`0.0.0.0:9187`)

## Example playbook

```yaml
---
- hosts: myhost
  roles: postgres-exporter
```

## License

MIT. See LICENSE for more details.

## Author Information

See my other Ansible roles at [angristan/ansible-roles](https://github.com/angristan/ansible-roles).
