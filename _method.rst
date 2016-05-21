 

Authentication
~~~~~~~~~~~~~~

You authenticate to the Stripe API by providing one of your API keys in
the request. You can manage your API keys from your
`account <https://dashboard.stripe.com/account>`__. You can have
multiple API keys active at one time. Your API keys carry many
privileges, so be sure to keep them secret!

``           curl               https://api.stripe.com/v1/charges \ -u               sk_test_BQokikJOvBiI2HlWgH4olfQ2:require               "stripe" Stripe.api_key = "sk_test_BQokikJOvBiI2HlWgH4olfQ2"import               stripe stripe.api_key = "sk_test_BQokikJOvBiI2HlWgH4olfQ2"require_once('./lib/Stripe.php');               Stripe::setApiKey("sk_test_BQokikJOvBiI2HlWgH4olfQ2");Stripe.apiKey = "sk_test_BQokikJOvBiI2HlWgH4olfQ2";           var               stripe = require("stripe")( "sk_test_BQokikJOvBiI2HlWgH4olfQ2"               );stripe.Key =               "sk_test_BQokikJOvBiI2HlWgH4olfQ2"         ``

kk

A sample test API key has been provided in all the examples on the page,
so you can test out any example right away.

 

Errors
------

Stripe uses conventional HTTP response codes to indicate success or
failure of an API request. In general, codes in the 2xx range indicate
success, codes in the 4xx range indicate an error that resulted from the
provided information (e.g. a required parameter was missing, a charge
failed, etc.), and codes in the 5xx range indicate an error with
Stripe's servers.

Not all errors map cleanly onto HTTP response codes, however. When a
request is valid but does not complete successfully (e.g. a card is
declined), we return a 402 error code.

Attributes
          

type
    The type of error returned. Can be ``invalid_request_error``,
    ``api_error``, or ``card_error``.
message
    A human-readable message giving more details about the error. For
    card errors, these messages can be shown to your users.
code
    optional For card errors, a short string from amongst those listed
    on the right describing the kind of card error that occurred.
param
    optional The parameter the error relates to if the error is
    parameter-specific. You can use this to display a message near the
    correct form field, for example.

HTTP Status Code Summary
~~~~~~~~~~~~~~~~~~~~~~~~

-  **200** OK - Everything worked as expected.
-  **400** Bad Request - Often missing a required parameter.
-  **401** Unauthorized - No valid API key provided.
-  **402** Request Failed - Parameters were valid but request failed.
-  **404** Not Found - The requested item doesn't exist.
-  **500, 502, 503, 504** Server errors - something went wrong on
   Stripe's end.

Errors
~~~~~~

Types
     

+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| invalid\_request\_error   | Invalid request errors arise when your request has invalid parameters.                                                                                      |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| api\_error                | API errors cover any other type of problem (e.g. a temporary problem with Stripe's servers) and should turn up only very infrequently.                      |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| card\_error               | Card errors are the most common type of error you should expect to handle. They result when the user enters a card that can't be charged for some reason.   |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+

Codes
     

incorrect\_number

The card number is incorrect.

invalid\_number

The card number is not a valid credit card number.

invalid\_expiry\_month

The card's expiration month is invalid.

invalid\_expiry\_year

The card's expiration year is invalid.

invalid\_cvc

The card's security code is invalid.

expired\_card

The card has expired.

incorrect\_cvc

The card's security code is incorrect.

incorrect\_zip

The card's zip code failed validation.

card\_declined

The card was declined.

missing

There is no card on a customer that is being charged.

processing\_error

An error occurred while processing the card.

rate\_limit

An error occurred due to requests hitting the API too quickly. Please
`let us know <https://support.stripe.com/email>`__ if you're
consistently running into this error.

CVC validation and zip validation can be enabled/disabled in your
`settings <https://dashboard.stripe.com/account>`__.

Handling errors
~~~~~~~~~~~~~~~

Our API bindings can raise exceptions for many reasons, such as a failed
charge, invalid parameters, authentication errors, and network
unavailability. We recommend always trying to gracefully handle
exceptions from our API.

Our API bindings can produce errors for many reasons, such as a failed
charge, invalid parameters, authentication errors, and network
unavailability.
