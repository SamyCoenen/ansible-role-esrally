Ansible Role: Rally
=========

[![Build Status](https://travis-ci.org/samycoenen/ansible-role-esrally.svg?branch=master)](https://travis-ci.org/samycoenen/ansible-role-esrally)

Install Rally, the benchmarking tool for Elasticsearch from Elastic. Compatible with RHEL/CentOS, Debian/Ubuntu servers.

Requirements
------------

You will need pip, which should already be installed.

Role Variables
--------------

    git_folder: "/tmp/esrally"
    config_version: "8"
    env_name: "rally"
    java8_home: "/usr/lib/jvm/java-8-openjdk-amd64"
    #local.dataset.cache: "${node:root.dir}/data"
    datastore_type: "elasticsearch"
    datastore_host: "localhost"
    datastore_port: "80"
    datastore_secure: "False"
    datastore_user: ""
    datastore_password: ""
    default_track_url: "https://github.com/elastic/rally-tracks"
    preserve_benchmark_candidate: "True"

Dependencies
------------

  - geerlingguy.java
  - shelleg.gradle

Example Playbook
----------------

    - hosts: servers
      vars:
        datastore_host: elasticsearch.example.com
      roles:
         - samycoenen.ansible-role-esrally

License
-------

EUPL v1.2

Author Information
------------------


This role was created in 2017 by [Samy Coenen](https://www.samycoenen.be/).
