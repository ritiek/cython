This custom v3.10.10 branch makes the ``del`` keyword do nothing.

Compiling
---------

.. code-block:: bash

    $ ./configure --prefix=$(pwd)/result --with-pydebug --enable-shared
    $ make -j8
    $ make install

Experimenting
-------------

.. code-block:: bash

    $ cd result/bin
    $ ln -sf python3.10 python
    $ LD_LIBRARY_PATH="$(pwd)/../lib/" ./python

.. code-block:: python

    >>> a = 10
    >>> del a
    >>> a
    10
