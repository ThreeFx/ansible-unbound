unbound
=========

Installs and configures unbound as recursive, caching resolver.

Requirements
------------

None.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
 `unbound_listen_ips`| [] | **required**, ip addresses to listen on
 `unbound_outgoing_ips`| `"{{ unbound_listen_ips }}"`
 `unbound_allow_subnets`| [] | optional, allowed subnets for querying unbound
 `unbound_stub_zones`| [] | optional, stub zones to configure, see `defaults/main.yml` for details
 `unbound_v4_reverse_zones`| [] | optional, IPv4 reverse zones to configure, see `defaults/main.yml` for details

Dependencies
------------

## Optional

Works well with my [dhcp-ddns](https://github.com/ThreeFx/ansible-dhcp-ddns) for
configuring a resolver which respects DHCP DDNS entries. In this case be careful
that the domain configured in the `dhcp-ddns` role and here match exactly.

Example Playbook
----------------

See `molecule/default/main.yml`.

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
