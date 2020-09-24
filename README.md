RPIREPORTER role
=========

This is a role created to easily install RPi-Reporter-MQTT2HA-Daemon on the RPis.

More details can be found on the github: https://github.com/ironsheep/RPi-Reporter-MQTT2HA-Daemon

Requirements
------------

For updated script requirements please read the developer GitHub.

Ansible details
----------------

**APT package** 

Using a loop in apt module is deprecated and will be removed in version 2.11. Instead of using the loop and specifying name: {{ item }}, you can pass an array to the name key and specify the items like this:

    - apt: 
      - name: 
        - git 
        - python3 
        - python3-pip 
        - python3-tzlocal 
        - python3-sdnotify 
        - python3-colorama 
      - state: latest

Role Variables
--------------

This roles uses the following variables to configure the MQTT enviroment. The variables are configured in /vars/main.yaml

    hostname = {{ mqtt_hostname }}
    username = {{ mqtt_username }}
    password = {{ mqtt_password }}


Dependencies
------------

For updated script dependendies please read the developer GitHub.


Example Playbook
----------------

    - hosts: rpi
      become: yes
      roles:
         - rpireporter


Author Information
------------------

Pedro Ferreira
