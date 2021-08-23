# Ansible Role: ansible-apps_haproxy_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_haproxy_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_haproxy_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_haproxy_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_haproxy_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_haproxy_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_haproxy_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_haproxy_exporter.svg)](https://github.com/lotusnoir/ansible-apps_haproxy_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_haproxy_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_haproxy_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_haproxy_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_haproxy_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_haproxy_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_haproxy_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_haproxy_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_haproxy_exporter)


Deploy [haproxy_exporter](https://github.com/prometheus/haproxy_exporter) to expose haproxy metrics to prometheus.

## Role variables

| Name                             | Default Value  | Description                        |
| -------------------------------- | -------------- | -----------------------------------|
| `haproxy_exporter_version`       | 1.2.0          | haproxy_exporter version |
| `haproxy_exporter_type`          | 1.2.0          | haproxy_exporter version |
| `haproxy_exporter_temp_dir`      | /tmp           | temporary directory to uncompress package |
| `haproxy_exporter_install_dir`   | /usr/local/bin | directory to install binary |
| `haproxy_exporter_force_install` | false          | force install variable |
| `haproxy_exporter_user`          | 9102           | systemd user |
| `haproxy_exporter_group`         | 9102           | systemd group |
| `haproxy_exporter_port`          | 9102           | port to expose |
| `haproxy_exporter_metrics_path`  | 9102           | metrics path |
| `haproxy_exporter_scrape_uri`    | 9102           | haproxy stats uri |
| `haproxy_exporter_timeout`       | 9102           | exporter timeout |
| `haproxy_exporter_log_level`     | 9102           | exporter log level |
| `haproxy_exporter_log_format`    | 9102           | exporter log format |

## Examples

	---
	- hosts: apps_haproxy_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_haproxy_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13572](https://grafana.com/grafana/dashboards/13572)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
