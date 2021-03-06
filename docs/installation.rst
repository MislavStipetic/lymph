:tocdepth: 1

Installation
============

Installing lymph itself (for Python 2.7 or 3.4) is as simple as:

.. code:: bash

    pip install lymph

Yet, in order to make full use of lymph you'll also need to install lymph's dependencies: 
`ZooKeeper`_ (for service discovery) and `RabbitMQ`_ (for events) and have them
running.

If these are already set up, you can skip straight and continue the next
chapter.


Installing dependencies
~~~~~~~~~~~~~~~~~~~~~~~

The RabbitMQ server's default configuration is enough for development and
testing.  For detailed information on how to configure ZooKeeper refer to the
`ZooKeeper`_ webpage and the `Getting Started Guide`_. However, it's default
configuration should also be enough.


On Ubuntu
---------

If you haven't already install Python essentials:

.. code:: bash

	$ sudo apt-get install build-essential python-dev python-pip

Install and start ZooKeeper using:

.. code:: bash

	$ sudo apt-get install zookeeper zookeeperd
	$ sudo service zookeeper start
    
ZooKeeper's configuration file is located at ``/etc/zookeeper/conf/zoo.cfg``.

Install and start the RabbitMQ server:

.. code:: bash

    $ sudo apt-get install rabbitmq-server
    $ sudo service rabbitmq-server start


On OSX
------

Install RabbitMQ and ZooKeeper:

.. code:: bash

    $ brew install rabbitmq zookeeper

ZooKeeper's configuration file is located at
``/usr/local/etc/zookeeper/zoo.cfg``.


.. _ZooKeeper: http://zookeeper.apache.org
.. _RabbitMQ: http://www.rabbitmq.com/
.. _Getting Started Guide: http://zookeeper.apache.org/doc/trunk/zookeeperStarted.html
.. _tox: https://testrun.org/tox/latest/
