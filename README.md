[![Build Status](https://travis-ci.org/a0s/ansible-role-hostapd.svg?branch=master)](https://travis-ci.org/a0s/ansible-role-hostapd)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-a0s.hostapd-blue.svg)](https://galaxy.ansible.com/a0s/hostapd)

hostapd
=======

Install and setup hostapd. 

Role Variables
--------------

`hostapd_conf` (default:[]): list of lines to put in /etc/hostapd.conf

`hostapd_default` (default: "/etc/default/hostapd"): path to default config

`hostapd_default_daemon_conf` (default: "/etc/hostapd.conf"): path to daemon's config

`hostapd_default_daemon_opts` (default: ""): daemon's options

Example Playbook
----------------

    - hosts: servers
      roles:
         - a0s.hostapd
      vars:
        hostapd_conf:
          - |
            interface=wlan0
            hw_mode=g
            channel=10
            ieee80211d=1
            country_code=EU
            ieee80211n=1
            wmm_enabled=1
            ssid=somename
            auth_algs=1
            wpa=2
            wpa_key_mgmt=WPA-PSK
            rsn_pairwise=CCMP
            wpa_passphrase=somepassword


Useful links
------------

[Gentoo's page about hostapd](https://wiki.gentoo.org/wiki/Hostapd)

License
-------

MIT
