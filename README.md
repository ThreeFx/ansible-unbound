unbound
=========

Installs and configures a basic unbound instance.

Requirements
------------

Works well with [dhcp-ddns](https://github.com/ThreeFx/ansible-dhcp-ddns) for
delegating queries.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
 `unbound_listen_ips`| [] | **required**, ip addresses to listen on
 `unbound_outgoing_ips`| `"{{ unbound_listen_ips }}"`
 `unbound_allow_subnets`| [] | optional, allowed subnets for querying unbound
 `unbound_domain`| "" | optional, local domain for which to forward requests
 `unbound_private_dns_servers`| [] | optional, local DNS servers to query for `{{ unbound_domain }}`

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in
regards to parameters that may need to be set for other roles, or variables that
are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: unbound, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a
website (HTML is not allowed).
