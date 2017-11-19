=============
Configuration
=============

To install this module, just you need to install following module: payment_checkout

After install the module 

* Go to Website Admin > Configuration > Settings :

.. image:: ../images/check_setting.PNG

* Add your API Access Key :

.. image:: ../images/check_config.PNG


* Configuration :

Test environment

.. image:: ../images/check_config_2.PNG

Once the payment method ready, make it visible in the payment interface and activate the Production mode.

Shop
====

* Choose checkout.com

.. image:: ../images/choose_checkout.PNG


* Test card validity

**Enter Card Details**

.. image:: ../images/test_card.PNG

If Invalid Card Details Checkout error message until the card will be valid and the button checkout now will be appear.
 
* Card Valid

Once the customer completes and submits his payment details, if the card tokenisation is successful the Checkout.js payment lightbox will appear as follows:

.. image:: ../images/test_card_valid.PNG


Transaction
===========

* Transaction Invalid

.. image:: ../images/INVALID_transaction.PNG

If an error occurred in charging the card, check the status, responseMessage in the response for information regarding the cause of the error

* Transaction Valid

The transaction has been approved by the Issuer and the amount is held on the customer’s card.

.. image:: ../images/order_valid.PNG


* Transaction Sandbox : Transaction Details

.. image:: ../images/sandbox_transaction.PNG


* Transaction Odoo : Transaction Details :

.. image:: ../images/sale_order_transaction.PNG
