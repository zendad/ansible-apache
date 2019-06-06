# Ansible Role: Apache 2.4

An Ansible Role that installs Apache 2.4 on RHEL/CentOS or Amazonlinux.

## Requirements
SSL  certificate and key files if you have SSL/TLS enabled

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    apache_enablerepo: ""

The repository to use when installing Apache (only used on RHEL/CentOS systems). If you'd like later versions of Apache than are available in the OS's core repositories, use a repository like EPEL (which can be installed with the `geerlingguy.repo-epel` role).

    apache_listen_ip: "*"
    apache_listen_port: 80
    apache_listen_port_ssl: 443

The IP address and ports on which apache should be listening. Useful if you have another service (like a reverse proxy) listening on port 80 or 443 and need to change the defaults.

    apache_create_vhosts: true
    apache_vhosts_filename: "v1.conf"
    apache_vhosts_template: "vhosts.conf.j2"