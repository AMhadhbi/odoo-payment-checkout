=========================
Odoo eCommerce
=========================
Odoo embeds several payment methods to get paid on eCommerce, Sales and Invoicing apps.

Payment acquirers
=================

* Redirect the customers to payment platforms to collect money effortless and track the payment status (call-back). 
* Call back with payment status
* Store card to quickly pay next orders
* Authorize the payment capture

Odoo supports more and more platforms over time:

* Paypal
* Ingenico
* Authorize.net
* Adyen
* Buckaroo
* PayUmoney
* Sips
* Stripe


Transaction managment
=====================

Odoo confirms orders automatically as soon as the payment is authorized by a payment acquirer. 

* **Draft**: transaction under processing.

* **Pending**: the payment acquirer keeps the transaction on hold and you need to authorize it from the acquirer interface.

* **Authorized**: the payment has been authorized but not yet captured. 

* **Done**: the payment is authorized and captured. The order has been confirmed.

* **Error**: an error has occured during the transaction. The customer needs to retry the payment. The order is still in draft.

* **Cancelled**: when the customer cancels the payment in the payment acquirer form. They are taken back to Odoo in order to modify the order.



The steps to do this are detailed here:
https://www.odoo.com/documentation/user/11.0/ecommerce/shopper_experience/payment_acquirer.html