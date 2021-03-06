API documentation
=================

This is the API documentation for DynamoDB Config Store.

DynamoDBConfigStore
-------------------

.. autoclass:: dynamodb_config_store.DynamoDBConfigStore
    :private-members:
    :members:

ConfigStores
------------

ConfigStore
~~~~~~~~~~~

This is the ``ConfigStore`` base class that all other config stores inherit from.

.. autoclass:: dynamodb_config_store.config_stores.ConfigStore
    :private-members:
    :members:

DirectConfigStore
~~~~~~~~~~~~~~~~~

The ``DirectConfigStore`` is the default Config Store. All requests made will be send directly to DynamoDB so that the latest configuration is fetched at all times.

.. autoclass:: dynamodb_config_store.config_stores.direct.DirectConfigStore
    :private-members:
    :members:

TimeBasedConfigStore
~~~~~~~~~~~~~~~~~~~~

The ``TimeBasedConfigStore`` is a Config Store used for fetching configuration from DynamoDB on a preset interval. All configuration options will be exposed using instance attributes such as ``store.config.option``, where ``option`` is the store option.

This class shall not be instanciated directly, it's called by ``DynamoDBConfigStore``.

.. autoclass:: dynamodb_config_store.config_stores.time_based.TimeBasedConfigStore
    :private-members:
    :members:

Exceptions
----------

.. automodule:: dynamodb_config_store.exceptions
    :members:
