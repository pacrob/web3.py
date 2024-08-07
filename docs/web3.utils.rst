Utils
=====

.. py:module:: web3.utils

The ``utils`` module houses public utility functions and classes.

ABI
---

.. automodule:: web3.utils.abi
   :members:
   :undoc-members:
   :show-inheritance:

Address
-------

.. py:method:: utils.get_create_address(sender, nonce)

    Return the checksummed contract address generated by using the ``CREATE`` opcode by
    a sender address with a given nonce.


.. py:method:: utils.get_create2_address(sender, salt, init_code)

    Return the checksummed contract address generated by using the ``CREATE2`` opcode by
    a sender address with a given salt and contract bytecode. See
    `EIP-1014 <https://eips.ethereum.org/EIPS/eip-1014>`_.


Caching
-------

.. py:class:: utils.SimpleCache

    The main cache class being used internally by web3.py. In some cases, it may prove
    useful to set your own cache size and pass in your own instance of this class where
    supported.


Exception Handling
------------------

.. py:method:: utils.handle_offchain_lookup(offchain_lookup_payload, transaction)

    Handle ``OffchainLookup`` reverts on contract function calls manually. For an example, see :ref:`ccip-read-example`
    within the examples section.


.. py:method:: utils.async_handle_offchain_lookup(offchain_lookup_payload, transaction)

    The async version of the ``handle_offchain_lookup()`` utility method described above.
