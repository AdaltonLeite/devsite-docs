# Integrate Checkout Pro

The integration with Checkout Pro allows you to charge via our web form from any device in a simple, fast and secure way.

In this documentation you will find all the necessary steps to integrate Checkout Pro through **our SDKs**. To do this, follow the steps described below.


> It is also possible to perform the integration through calls via backend directly to the [Preferences API](/developers/en/reference/preferences/_checkout_preferences/post). In this template, you will get the Checkout Pro link in the `init_point` attribute, in the API request response. From there, just use it to redirect the buyer to the checkout.



## Install Mercado Pago SDK

The first step to integrate Checkout Pro is to install the Mercado Pago SDK in your project. To do this, use one of the codes available below.


[[[
```php
===
To install the SDK, you must run the following code in your terminal command line using [Composer](https://getcomposer.org/download):
===
php composer.phar require "mercadopago/dx-php"
```
```node
===
To install the SDK, you must run the following code in your terminal command line using [npm](https://www.npmjs.com/get-npm):
===
npm install Mercadopago
```
```java
===
To install the SDK in your [Maven](http://maven.apache.org/install.html) project, you must add the following dependency to your <code>pom.xml</code> file and run the code < code>maven install</code> in your terminal command line:
===
<dependency>
<groupId>com.mercadopago</groupId>
<artifactId>sdk-java</artifactId>
<version>2.0.0</version>
</dependency>
```
```ruby
===
To install the SDK, you must run the following code in your terminal command line using [gem](https://rubygems.org/gems/mercadopago-sdk):
===
gem install Mercadopago-sdk
```
```csharp
===
----[mlb]----
To install the SDK, you must run the following code in the command line of your terminal using [NuGet](https://docs.microsoft.com/en-us/nuget/reference/nuget-exe-cli-reference):

------------

----[mla, mlm, mco, mlc, mlu]----
To install the SDK, you must run the following code in the command line of your terminal using [NuGet](https://docs.microsoft.com/es-es/nuget/reference/nuget-exe-cli-reference):

------------
===
nuget install Mercadopago-sdk
```
```python
===
To install the SDK, you must run the following code in the command line of your terminal using [pip](https://pypi.org/project/mercadopago/):
===
pip3 install MercadoPago
```
]]]



> SERVER_SIDE
>
> h2
>
> Create preference

Preferences are sets of information that allow you to configure a product or service that you want to charge, such as price and quantity, as well as other settings related to the defined payment flow.

To create a preference, use one of the SDKs available below, filling in the attributes with the respective information.



[[[
```php
<?php
// Mercado Pago SDK
require __DIR__ .  '/vendor/autoload.php';
// Add Your credentials
MercadoPago\SDK::setAccessToken('PROD_ACCESS_TOKEN');
?>
```
```node
// Mercado Pago SDK
const mercadopago = require ('mercadopago');
// Add Your credentials
mercadopago.configure({
  access_token: 'PROD_ACCESS_TOKEN'
});
```
```java
// Mercado Pago SDK
import com.mercadopago.MercadoPagoConfig;
// Add Your credentials
MercadoPagoConfig.setAccessToken("PROD_ACCESS_TOKEN");
```
```ruby
# Mercado Pago SDK
require 'mercadopago'
# Add Your credentials
sdk = Mercadopago::SDK.new('PROD_ACCESS_TOKEN')
```
```csharp
// Mercado Pago SDK
 using MercadoPago.Config;
 // Add Your credentials
MercadoPagoConfig.AccessToken = "PROD_ACCESS_TOKEN";
```
```python
# Mercado Pago SDK
import mercadopago
# Add Your credentials
sdk = mercadopago.SDK("PROD_ACCESS_TOKEN")
```
]]]


When you finish creating the preference, you need to configure it according to your product or service. To do so, use one of the codes available below, filling in the attributes with the respective information.


----[mla, mlb, mlu, mpe, mlm]----

[[[
 ```php
<?php
// Create a preference object
$preference = new MercadoPago\Preference();

// Create a preference item
$item = new MercadoPago\Item();
$item->title = 'My Item';
$item->quantity = 1;
$item->unit_price = 75.56;
$preference->items = array($item);
$preference->save();
?>
```
```node
// Create a preference object
let preference = {
  items: [
    {
      title: 'My Item',
      unit_price: 100,
      quantity: 1,
    }
  ]
};

mercadopago.preferences.create(preference)
.then(function(response){
// This value replaces the String "<%= global.id %>" in your HTML
  global.id = response.body.id;
}).catch(function(error){
  console.log(error);
});
```
```java
// Create a preference object
PreferenceClient client = new PreferenceClient();

// Create a preference item
List<PreferenceItemRequest> items = new ArrayList<>();
PreferenceItemRequest item =
   PreferenceItemRequest.builder()
       .title("Meu produto")
       .quantity(1)
       .unitPrice(new BigDecimal("100"))
       .build();
items.add(item);

PreferenceRequest request = PreferenceRequest.builder().items(items).build();

client.create(request);
```
```ruby
# Create a preference request
preference_data = {
  items: [
    {
      title: 'My Item',
      unit_price: 75.56,
      quantity: 1
    }
  ]
}
preference_response = sdk.preference.create(preference_data)
preference = preference_response[:response]

# This value replaces the String "<%= @preference_id %>" in your HTML
@preference_id = preference['id']
```
```csharp
// Create the preference request object
var request = new PreferenceRequest
{
    Items = new List<PreferenceItemRequest>
    {
        new PreferenceItemRequest
        {
            Title = "My Item",
            Quantity = 1,
            CurrencyId = "[FAKER][CURRENCY][ACRONYM]",
            UnitPrice = 75.56m,
        },
    },
};

// Create the preference using the client
var client = new PreferenceClient();
Preference preference = await client.CreateAsync(request);
```
```python
# Create a preference item
preference_data = {
    "items": [
        {
            "title": "My Item",
            "quantity": 1,
            "unit_price": 75.76
        }
    ]
}

preference_response = sdk.preference().create(preference_data)
preference = preference_response["response"]
```
]]]


------------

----[mlc, mco]----

[[[
 ```php
<?php
// Create a preference object
$preference = new MercadoPago\Preference();

// Create a preference item
$item = new MercadoPago\Item();
$item->title = 'My Item';
$item->quantity = 1;
$item->unit_price = 75;
$preference->items = array($item);
$preference->save();
?>
```
```node
// Create a preference object
let preference = {
  items: [
    {
      title: 'My Item',
      unit_price: 100,
      quantity: 1,
    }
  ]
};

mercadopago.preferences.create(preference)
.then(function(response){
// This value replaces the String "<%= global.id %>" in your HTML
  global.id = response.body.id;
}).catch(function(error){
  console.log(error);
});
```
```java
// Create a preference object
Preference preference = new Preference();

// Create a preference item
Item item = new Item();
item.setTitle("My Item")
    .setQuantity(1)
    .setUnitPrice((float) 75);
preference.appendItem(item);
preference.save();
```
```ruby
# Create a preference request
preference_data = {
  items: [
    {
      title: 'My Item',
      unit_price: 75,
      quantity: 1
    }
  ]
}
preference_response = sdk.preference.create(preference_data)
preference = preference_response[:response]

# This value replaces the String "<%= @preference_id %>" in your HTML
@preference_id = preference['id']
```
```csharp
// Create the preference request object
var request = new PreferenceRequest
{
    Items = new List<PreferenceItemRequest>
    {
        new PreferenceItemRequest
        {
            Title = "My Item",
            Quantity = 1,
            CurrencyId = "[FAKER][CURRENCY][ACRONYM]",
            UnitPrice = 75m,
        },
    },
};

// Create the preference using the client
var client = new PreferenceClient();
Preference preference = await client.CreateAsync(request);
```
```python
# Create a preference object
preference_data = {
    "items": [
        {
            "title": "My Item",
            "quantity": 1,
            "unit_price": 75
            
        }
    ]
}

preference_response = sdk.preference().create(preference_data)
preference = preference_response["response"]
```
]]]


> WARNING
>
> Important
>
> The value of `unit_price` must be an integer.

------------


> CLIENT_SIDE
>
> h2
>
> Add Checkout


Once you have created the preference in your backend, you will need to install the Mercado Pago frontend SDK to your project in order to add the Checkout Pro button.

The installation is done in **two steps**: adding the Mercado Pago SDK to the project with your configured credentials and starting the checkout from the previously generated preference.



1. To include the Mercado Pago.js SDK, add the code below to the project's HTML.


```html
// SDK MercadoPago.js
<script src="https://sdk.mercadopago.com/js/v2"></script>
```

2. When you finish adding the Mercado Pago.js SDK, **configure the SDK credentials** and initialize your checkout with the **ID of the previously** created preference and the identifier of the element where the payment button should be displayed, as shown in the example below.


[[[
```html
<div class="cho-container"></div>
<script>
const mp = new MercadoPago('PUBLIC_KEY', {
locale: 'pt-BR'
});

mp.checkout({
preference: {
id: 'YOUR_PREFERENCE_ID'
},
render: {
container: '.cho-container',
label: 'Pay',
}
});
</script>
```
]]]

> NOTE
>
> Important
>
> Remember to replace the value `BR` to your country on `locale` field.

In the example above, a payment button will be rendered and will be responsible for opening Checkout Pro. If you want to customize the way the checkout will be opened, see the section [Opening Schema](/developers/en/docs/checkout-pro/checkout-customization/user-interface/opening-schema)


## Implementation example

Check out the [full integration example](http://github.com/mercadopago/checkout-payment-sample) on GitHub for **PHP** or **NodeJS** to _download_ a basic project for quick implementation from Checkout Pro.
