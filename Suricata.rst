Suricata
========

From https://suricata-ids.org:

    Suricata is a free and open source, mature, fast and robust network
    threat detection engine. Suricata inspects the network traffic using
    a powerful and extensive rules and signature language, and has
    powerful Lua scripting support for detection of complex threats.

Performance
-----------

We compile Suricata to support both `PF\_RING <PF_RING>`__ and `<AF-PACKET>`_ to allow you to spin up multiple workers to handle more traffic.  Modern versions of Setup default to `<AF-PACKET>`_.

| For high traffic levels, you may want to pin Suricata to specific CPU cores using the affinity settings in ``suricata.yaml``:
| https://suricata.readthedocs.io/en/latest/configuration/suricata-yaml.html#threading

Configuration
-------------

| You can configure Suricata via suricata.yaml:
| ``/etc/nsm/HOSTNAME-INTERFACE/suricata.yaml``
| (where HOSTNAME is your actual hostname and INTERFACE is your actual sniffing interface)

If you would like to configure/manage IDS rules, please see:

`<Rules>`__

`<ManagingAlerts>`__

Logging
-------

| If you need to troubleshoot Suricata, check ``suricata.log``:
| ``/var/log/nsm/HOSTNAME-INTERFACE/suricata.log``
| (where HOSTNAME is your actual hostname and INTERFACE is your actual sniffing interface)

Stats
-----

| For detailed Suricata statistics, check ``stats.log``:
| ``/nsm/sensor_data/HOSTNAME-INTERFACE/stats.log``
| (where HOSTNAME is your actual hostname and INTERFACE is your actual sniffing interface)

More Information
----------------

| For more information about Suricata, please see:
| https://suricata-ids.org/
