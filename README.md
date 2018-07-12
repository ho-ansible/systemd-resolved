# Ansible role: systemd-resolved
Local caching DNS resolver

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `preferred_dns`: IP address of primary DNS server
+ `fallback_dns`: IP address of DNS server to use *only* if no other servers (e.g., per-interface) are configured
+ `default_domain` (default: none): domain to append to bare hostnames

## Dependencies
None.

## Example Playbook

```
- hosts: all
  roles:
    - { role: ho-ansible.systemd-resolved }
```

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/
