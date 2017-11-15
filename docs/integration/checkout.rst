=============
 Checkout.com
=============


* A streamlined payment solution

* Checkout.com’s end-to-end payment technology eliminates intermediaries, while data-rich insights track performance and drive approvals.

* Checkout.com offers two browser-based payment solutions that are suitable for non-PCI compliant merchants, Frames and Checkout.js.

Setting Up a Test Merchant Account
==================================

* You have to create Sandbox account in checkout.com as a sandbox user.

* To obtain the publicKey, kindly log in to the dashboard.

* Go to settings (gear icon of the top right corner), from there you should go to channel settings.

.. image:: ../images/sandbox_key.PNG

* You should find the keys at this point.


Checkout.js
============

The Checkout.js solution will allow to create a card token, and then charge the customer from the server using the generated card token. 

The steps to do this are detailed here:
https://docs.checkout.com/getting-started/checkout-js/charge-via-card-token

Charge with card token API call: 
https://docs.checkout.com/reference/merchant-api-reference/charges/charge-with-card-token 
 
The card token obtained in the cardTokenised event is a single-use token and no charge will be created until you do a charge with card token from the server's backend using merchant API.
Also, note that the real value you want to charge customers needs to originate from the backend and not from the configuration of the JS. 
The value inside the JS is only used for display purposes inside the lightbox.

Here is a sample code you can use to build on for the frontend configuration of Checkout.js :

Code::

	<form class="payment-form" method="POST" action="https://merchant.com/successUrl">
    <script>
        window.CKOConfig = {
            publicKey: 'pk_test_6ff46046-30af-41d9-bf58-929022d2cd14',
            customerEmail: 'user@email.com',
            value: 100,
            currency: 'GBP',
            cardFormMode: 'cardTokenisation',
            paymentMode: 'cards',
            cardTokenised: function(event) {
                    console.log(event.data.cardToken);
                    document.getElementsByClassName('payment-form')[0].submit();
                },
            };
    </script>
    <script async src="https://cdn.checkout.com/sandbox/js/checkout.js"></script>
	</form>
	

And here's a link to the https://docs.checkout.com/reference/checkout-js-reference/configuration-options reference if you wish to customise it further.

Use the card token obtained in the cardTokenised event to make a charge with card token from the server.


