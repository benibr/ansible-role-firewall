# ansible-role-firewall

This role sets a baisc iptables based firewall up using a bash script run by systemd.

Yes this is the 2000th implementation of such a firewall but I like to keep controll over this kinda stuff. k thx bye

## Example
```
    firewall:
      output_policy: ACCEPT
      allow:
        input:
          tcp:
            - 22
            - 143
            - 443
            - 587
            - 5222
            - 5269
          udp:
            - 69
      raw:
        - "-A INPUT -i ve-+ -j ACCEPT"
```
