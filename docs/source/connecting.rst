Connecting to the cluster
=========================

The main way of connecting to a cluster or any server is through Secure Shell (`ssh`), which is executed via a terminal. Basic terminal skills are assumed here. A couple more complex options have been put in place.

SSH
---
A regular `ssh` command looks like this
.. code-block:: bash

   ssh server.cvc.es

   # Using a certain username
   ssh youruser@server.cvc.es

   # Using a certain username and port
   ssh youruser@server.cvc.es -p 12345

In the CVC, the default port for `ssh` connections is `22345`, so don't forget to specify it in your command.

If you're inside the university network, domain names can also be used. If I were to connect to a server I could use the IP (`xxx.xxx.xxx.115`) or its more simple name
.. code-block:: bash
   ssh user@cudahpc15 -p 22345

You can avoid retyping your password by `setting up your private keys <https://www.redhat.com/sysadmin/passwordless-ssh>`_.

Even more, with OpenSSH you can make use of your `~/ssh/config` file for a more seamless connection. Check it `here <https://linuxize.com/post/using-the-ssh-config-file>`_ or just searching for `ssh config file`.

.. _remote-access:

Remote access
-------------
If you are outside of the university network and want to connect to a cluster or desktop computer in the CVC, connections are `not longer available <https://www.incibe-cert.es/en/early-warning/cybersecurity-highlights/cyber-attack-uab-servers-affects-its-digital-activity>`_.

But worry not, an SSH tunnel has been set to enable regular work again. First of all, connect with Héctor (hlaria@cvc...) for an account.

After that, only one more flag is needed in your `ssh` command
.. code-block:: bash

   ssh -J tunnel_user@tunnel_ip:22345 user@cudahcp15 -p 22345

and you should be able to work normally.

Guacamole portal
----------------

Web Service portal
------------------
