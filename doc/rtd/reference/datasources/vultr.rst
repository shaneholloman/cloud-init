.. _datasource_vultr:

Vultr
*****

The `Vultr`_ datasource retrieves basic configuration values from the locally
accessible instance metadata service. All data is served over HTTP from the
address ``169.254.169.254``. The endpoints are documented in the
`instance metadata service documentation`_.

Configuration
=============

Vultr's datasource can be configured as follows: ::

  datasource:
    Vultr:
      url: 'http://169.254.169.254'
      retries: 3
      timeout: 2
      wait: 2

* ``url``: The URL used to acquire the meta-data configuration.
* ``retries``: Determines the number of times to attempt to connect to the
  instance metadata service.
* ``timeout``: Determines the timeout (in seconds) to wait for a response from
  the instance metadata service.
* ``wait``: Determines the timeout (in seconds) to wait before retrying after
  accessible failure.

.. _Vultr: https://www.vultr.com/
.. _instance metadata service documentation: https://www.vultr.com/metadata/
