# 3proxy

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/3proxy/status.svg)](https://drone.osshelp.ru/ansible/3proxy)

The role for 3proxy installation and configuration.

## Usage (example)

```yaml
    - role: 3proxy
      proxy3_gateways:
        - { options: "-n -p12345 -a -i127.0.0.1" }
```

## Available parameters

### Main

Proxy gateway params:

| Param | Description |
| -------- | -------- |
| `proxy3_gateways` | Gateway services |
| `proxy3_gateways.[].type` | Default: `proxy`. proxy, socks, pop3p, ftppr, admin, dnspr, tcppm, udppm |
| `proxy3_gateways.[].options` | Gateway options |
| `proxy3_users` | Proxy users |
| `proxy3_users.[].name` | User name |
| `proxy3_users.[].pwtype` | Default: `CL`. CL - password is cleartext, CR - password is crypt-style password, NT - password is NT password (in hex) |
| `proxy3_users.[].password` | User password |

### Misc

Service params:

| Param | Description |
| -------- | -------- |
| `proxy3_version` | |
| `proxy3_binaries_url` | |
| `proxy3_binaries_sum` | |
| `proxy3_binaries_list` | |
| `proxy3_service_name` | |
| `proxy3_conf_dir` | |
| `proxy3_conf_path` | |
| `proxy3_passwd_path` | |
| `proxy3_binaries_dir` | |
| `proxy3_binary_path` | |
| `proxy3_pid_path` | |
| `proxy3_user` | |
| `proxy3_group` | |
| `proxy3_nservers` | |
| `proxy3_nscache` | |
| `proxy3_timeouts` | |
| `proxy3_auth` | |

## Useful links

- [Official documentation](https://3proxy.ru/doc/)

## TODO

- add user creation
- config generation improvements (e.g. enable auth based on var define, etc)
- role documentation
- role tests

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
