ansible-role-time
=========

Configure local time and NTP service.

Requirements
------------

This role has been tested on EL6 hosts.

Role Variables
--------------

__role\_time\_timezone__: The timezone for this host. Possible values found [here](http://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

```
role_time_timezone: 'America/New_York'
```

__role\_time\_ntp\_servers__: An array of NTP servers to query.

```
role_time_ntp_servers: [
'server 1.pool.ntp.org iburst',
'server 2.pool.ntp.org iburst',
'server 3.pool.ntp.org iburst'
]
```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  roles:
    - { role: bitmotive.ansible-role-time, tags: "time,common" }
```

License
-------

MIT
