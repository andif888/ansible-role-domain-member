# Ansible Role Domain Member
Joins Linux to AD using Ansible. 


### Operating systems

Tested with Ubuntu

## Example Playbook

For example

```yaml
- host: all
  vars:
    dns_domain_name: example.com                              # required
    domain_admin_user_short: administrator                    # required
    domain_admin_password: vagrant                            # required
    domain_admin_user_group: Domänen-Admins                   # optional
    ntp_client_ntp_server_ip:                                 # optional
      - 192.168.206.10
      - 192.168.223.10
    domain_ou_path: OU=Computers,OU=Infra,DC=example,DC=com   # optional
    
  roles:
    - ansible-role-domain-member
```

