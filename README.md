Uptime Kuma - Ansible
======================

This configuration repo installs the open-source tool [Uptime Kuma](https://github.com/louislam/uptime-kuma) on Ubuntu distributions (tested for 18.04 and 20.04).

After installation, the service will be available on `127.0.0.1:3001`. A reverse-proxy, such as NGINX or Caddy, can be used to route requests to this endpoint.

Role Variables
-------------

    kuma__user: kuma
    kuma__group: {{ kuma__user }}

    # Kuma requires node and npm. If nodejs is not installed, this flag can be used for quick installation of Node v14.
    kuma__install_nodejs: true
    nodejs__version: '14.x'