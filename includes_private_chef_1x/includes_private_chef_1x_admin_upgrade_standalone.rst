.. The contents of this file may be included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The installation process for a standalone upgrade of |chef private| does not reconfigure |chef private| or restart any of the services. This prevents inadvertent fail overs from occurring on High Availability installations.

On RedHat RPM based systems run rpm with the appropriate upgrade flags and with the new RPM to be installed:

.. code-block:: bash

   $ rpm -Uvh private-chef-1.1.10-1.el6.x86_64.rpm


.. warning:: When upgrading from |chef private| version 1.1.14 or earlier, a package script will delete ``/usr/bin/private-chef-ctl``. You can recreate it with:

.. code-block:: bash

   $ ln -sf /opt/opscode/embedded/cookbooks/bin/private-chef-ctl /usr/bin/


On |ubuntu| or |debian| deb-package based systems run |dpkg| with the install flag:

.. code-block:: bash

   $ dpkg -i private-chef_1.1.10-1.ubuntu.10.04_amd64.deb

After installing the upgraded package, you must instruct |private chef ctl| to update the configuration:

.. code-block:: bash

   $ private-chef-ctl upgrade

