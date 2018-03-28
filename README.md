Role Name
=========

Downloads and runs [Mock Server](http://www.mock-server.com)

Requirements
------------

None

Role Variables
--------------

To configure the actual mock server

```yaml
mock_server_server_port: 1080
```

Set this to listen for requests to mock. You must define either this and/or the proxy for the Mock Server to actually run

```yaml
mock_server_proxy_port: 1090
mock_server_proxy_remote_port: 80
mock_server_proxy_remote_host: localhost
```

The above sets up the pass-through proxy

Dependencies
------------

* geerlingguy.java

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: c0ntax.mock-server, mock_server_server_port: 1080 }

License
-------

Apache 2.0

