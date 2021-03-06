Gateway Snapshot
================

The gateway snapshot API allows to explicitly perform a snapshot through the gateway of one or more indices (backup them). By default, each index gateway periodically snapshot changes, though it can be disabled and be controlled completely through this API.


.. code-block:: js

    $ curl -XPOST 'http://localhost:9200/twitter/_gateway/snapshot'


Multi Index
-----------

The gateway snapshot API can be applied to more than one index with a single call, or even on **_all** the indices.


.. code-block:: js

    $ curl -XPOST 'http://localhost:9200/kimchy,elasticsearch/_gateway/snapshot'
    
    $ curl -XPOST 'http://localhost:9200/_gateway/snapshot'

