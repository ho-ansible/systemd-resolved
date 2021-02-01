# Ansible role: systemd-resolved
Local caching DNS resolver

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `preferred_dns`: IP address of primary DNS server
+ `fallback_dns`: IP address of DNS server to use *only* if no other servers (e.g., per-interface) are configured
+ `search_domains` (default: none): list of domains to append to bare hostnames

## Handlers
+ `use resolved`: sets `/etc/resolv.conf` to point only to local systemd-resolved at 127.0.0.53
+ `restart resolved`: restart systemd-resolved.service

## Playbooks
+ `main.yml`: apply role
+ `uninstall.yml`: remove. Run prior to removing host from inventory group.

## Dependencies
None.

## License
+ Ansible role licensed [MIT](LICENSE)

## Author Information
+ Ansible role by [Sean Ho](https://github.com/ho-ansible/)
