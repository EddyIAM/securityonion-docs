Firewall
========

Setup defaults to only allowing port 22 (ssh)
---------------------------------------------

Setup defaults to locking down the local ``ufw`` firewall to only allowing port 22 (ssh).  There is a note at the end of Setup that tells you this and lets you know that, if you need to allow connections on other ports, you can run the `<so-allow>`_ utility.

Sensors automatically add their own firewall rules to the master server
-----------------------------------------------------------------------

When you run Setup on a sensor-only installation, it will ssh to the master server and add new firewall rules to the master server to allow the sensor to connect on the following ports:

-  22/tcp (ssh)
-  4505/tcp (salt)
-  4506/tcp (salt)
-  7736/tcp (sguil)
