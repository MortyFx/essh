# essh

SSH Login Management Tool

![usage](./assets/essh.gif)

### Installation
```
go get -u github.com/seamounts/essh
```
If you don't have a Go environment, you can download the executable file directly: [binary.tar.gz](https://github.com/seamounts/essh/releases/download/v1.0.0/binary.tar.gz)

### Configuration

Create a file in your user directory: `.essh.yaml` or `essh.yaml`

The configuration format is as follows:

```yaml
- name: Login with SSH key
  user: root
  host: 1.2.3.4
  port: 22
  keypath: path-key

- name: Login with password
  user: root
  host: 5.6.7.8
  port: 22
  password: 123456

- name: Execute shell command after login
  user: root
  host: 10.2.3.4
  port: 22
  cmds:
    - cmd: ssh root@2.3.4.5

- name: Jump server
  user: root
  host: 10.10.101.1
  port: 22
  jump:
    - user: root
      host: 10.10.101.2
      port: 22
```
