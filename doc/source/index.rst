os_ceilometer Role Docs
=======================

The os_ceilometer role is used to to deploy, configure and install OpenStack
Telemetry.

This role will install the following:
    * ceilometer-api
    * ceilometer-registry

Basic Role Example
^^^^^^^^^^^^^^^^^^

.. code-block:: yaml

    - name: Install ceilometer server
      hosts: ceilometer_all
      user: root
      roles:
        - { role: "os_ceilometer", tags: [ "os-ceilometer" ] }
      vars:
        external_lb_vip_address: 172.16.24.1
        internal_lb_vip_address: 192.168.0.1
