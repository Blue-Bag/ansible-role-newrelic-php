newrelic-php
============

An Ansible role to setup New Relic PHP agent:
https://docs.newrelic.com/docs/php/new-relic-for-php


Requirements
------------

Ubuntu Trusty with PHP installed. This role tries to restart PHP-FPM and/or the Apache web server.

Notes:
List of newrelic IPs: https://docs.newrelic.com/docs/apm/new-relic-apm/getting-started/networks#availability
50.31.164.139	Chicago	Illinois
50.112.95.211	US West 2	Oregon
54.247.188.179	EU West 1	Ireland
54.248.250.232	AP Northeast 1	Japan
54.251.34.67	AP Southeast 1	Singapore
184.73.237.85	US East 1	Virginia
The following IP addresses are currently reserved for future availability monitoring use. Whitelist them for forward compatibility.
IP address	Region name	Location
50.16.189.130	US East 1	Virgina
50.18.57.7	US West 1	California
54.214.255.205	US West 2	Oregon
54.228.244.177	EU West 1	Ireland
54.232.123.139	SA East 1	Brazil
54.241.22.142	US West 1	California
54.248.225.67	AP Northeast 1	Tokyo
54.251.109.246	AP Southeast 1	Singapore
54.252.114.169	AP Southeast 2	Sydney
54.252.114.170	AP Southeast 2	Sydney
177.71.245.207	SA East 1	Brazil


Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows

    # License key (required)
    newrelic_license_key: ~

    # Application name (required)
    newrelic_appname: "{{ ansible_hostname }} PHP"


Dependencies
------------

Requires the New Relic repository to be set up; depends on [sivel.newrelic](https://github.com/sivel/ansible-newrelic) for this purpose.


License
-------

MIT

