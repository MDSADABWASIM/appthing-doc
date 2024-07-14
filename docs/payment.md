# Payment

We are giving you a ready-made payment gateway support for your app.

## Which payment gateways are supported?

- We are supporting **Stripe**, **Paypal** and **Cashfree** payment gateways.
- You can choose any of the above payment gateways and follow the instructions to integrate it in your app.

## Stripe setup

- Go to your stripe account and create a new product.
- Add your strip secret key in your .env file.

```
STRIPE_SECRET= 'your_stripe_secret_key'
```
- Add your merchant name in your .env file.

```
STRIPE_MERCHANT_NAME= 'your_merchant_name'
```

- If you encounter any error, please check the **[requirements section](https://pub.dev/packages/flutter_stripe#requirements)**
- Now you just need to call this function to make a payment from your **stripe_service** file:

``` dart

Future<void> stripeMakePayment({
required String userName, //Name of the user who is making the payment
required String userEmail, //Email of the user
required String userNumber, //Phone number of the user
required String amount, //Amount of the payment ('100', '500' etc.)
required String currency,//Currency of the payment ('USD', 'EUR', 'GBP' etc.)
})

```


## Paypal setup

- Go to your paypal account and create a new product.
- Add your paypal client id in your .env file.

```dart
PAYPAL_CLIENT_ID = 'your_paypal_client_id'
```
- If you encounter any error, please check the **[usage section](https://pub.dev/packages/flutter_paypal_native#usage)**
- Now you just need to call this function to make a payment from your **paypal_service** file:

``` dart
initPayPal()
```

- set these values as needed:

``` dart
returnUrl: // Add your return url here
currencyCode: FPayPalCurrencyCode.usd,  // Change to your currency code

```

- After payment you get these three callbacks to handle the payment:

``` dart
onSuccess: (data) {
  //successfully paid
},
onError: (data) {
  //an error occured
},
onShippingChange: (data) {
  //the user updated the shipping address
}

```

## Cashfree setup

- Add your cashfree client id and secret key in your .env file.

```dart
'CASHFREE_SECRET_KEY': 'your_cashfree_secret_key'
'CASHFREE_CLIENT_ID': 'your_cashfree_client_id'
```

- If you encounter any error, please check the **[usage section](https://docs.cashfree.com/docs/flutter-integration)**
- Now you just need to call this function to make a payment from your **cashfree_service** file:

- Step 1: call this function to initialize the cashfree service:

``` dart
  void makeRequest(
    double amount,
    String userId,
    String userName,
    String userEmail,
    String userPhone,
    String currency,
  )
```
- Step 2: once the makeRequest is called, you can call the **pay** function to make the payment:

``` dart
  pay()
```

- Step 3: you get two callbacks to handle the success and error of the payment:

``` dart
  onSuccess: (data) {
    //successfully paid
  }

  onError: (data) {
    //an error occured
  }
```

## Next step

Go to **[Cloud storage setup](cloud_storage.md)** section.

