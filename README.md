# Ansible role: systemd-resolved
Local caching DNS resolver

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `preferred_dns`: IP address of primary DNS server
+ `fallback_dns`: IP address of DNS server to use *only* if no other servers (e.g., per-interface) are configured
+ `search_domains` (default: none): list of domains to append to bare hostnames

## Dependencies
None.

## License
MIT

## Author Information
+ Ansible role by [Sean Ho](https://github.com/ho-ansible/)
