.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|chef solo| can load data from a data bag as long as the contents of that data bag are accessible from a directory structure that exists on the same machine as |chef solo|. The location of this directory is configurable using the ``data_bag_path`` option in the |solo rb| file. The name of each sub-directory corresponds to a data bag and each JSON file within a sub-directory corresponds to a data bag item. Search is not available in recipes when they are run with |chef solo|; use the ``data_bag()`` and ``data_bag_item()`` functions to access data bags and data bag items.

.. note:: Use the ``chef-solo-search`` cookbook library (developed by |opscode| community member "edelight" and available from |github|) to add data bag search capabilities to a |chef solo| environment: https://github.com/edelight/chef-solo-search.