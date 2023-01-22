# ansible-role-domain-member

Joins linux to AD domain

## Table of content

- [Default Variables](#default-variables)
  - [dns_domain_name](#dns_domain_name)
  - [domain_admin_password](#domain_admin_password)
  - [domain_admin_user_group](#domain_admin_user_group)
  - [domain_admin_user_short](#domain_admin_user_short)
  - [domain_member_allow_ssh_password_auth_for_users](#domain_member_allow_ssh_password_auth_for_users)
  - [domain_member_allow_userlogin_without_fqdn](#domain_member_allow_userlogin_without_fqdn)
  - [domain_member_pkgs](#domain_member_pkgs)
  - [domain_ou_path](#domain_ou_path)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### dns_domain_name

AD Domain to join

#### Default value

```YAML
dns_domain_name: domain.local
```

### domain_admin_password

password of the username to join domain

#### Default value

```YAML
domain_admin_password: ''
```

### domain_admin_user_group

AD group gets added to sudoers

### domain_admin_user_short

username to join domain

#### Default value

```YAML
domain_admin_user_short: administrator
```

### domain_member_allow_ssh_password_auth_for_users

Allow ssh password authentication for users

#### Default value

```YAML
domain_member_allow_ssh_password_auth_for_users: false
```

### domain_member_allow_userlogin_without_fqdn

Allow user login with short user name. Example: user1 instead of user1@domain.local

#### Default value

```YAML
domain_member_allow_userlogin_without_fqdn: true
```

### domain_member_pkgs

Required packages to install

#### Default value

```YAML
domain_member_pkgs:
  - realmd
  - sssd
  - sssd-tools
  - oddjob
  - oddjob-mkhomedir
  - adcli
  - samba-common-bin
  - libnss-sss
  - libpam-sss
  - packagekit
  - python3-pexpect
```

### domain_ou_path

join into a specific OU



## Dependencies

None.

## License

GPLv3

## Author

Hotzenplotz
