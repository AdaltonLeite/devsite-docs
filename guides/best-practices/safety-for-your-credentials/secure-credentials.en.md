# Keep your credentials safe

By integrating Mercado Pago solutions, you will handle sensitive data that you must protect from possible losses or vulnerabilities. This data can be your credentials, those of your integrations and those of your clients.

Credentials are unique passwords with which we identify an integration in your account. They are used to capture payments in online stores and other applications securely. To find out detailed information about credentials, go to [Credentials](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/resources/credentials).

We will show you how you can optimize the security of your integrations simply and quickly.

## Send the access token by header

Every time you make API calls, **send the Access Token via header** instead of via query param. This will allow you to protect your Access Token from being exposed to anyone outside of your integration.

For example, if you perform a GET to the _/users/me_ resource, it would look like this:

```curl
curl -H 'Authorization: Bearer APP_USR-12345678-031820-X-12345678' \
https://api.mercadolibre.com/users/me
```

> Always keep your credentials hidden and do not expose them in any parameters or on the public side of your integration.

## Renew your credentials periodically

We recommend you renew your credentials frequently to avoid possible vulnerabilities.

Renew your credentials in a simple way by following these steps:

1. Go to [Dashboard](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/panel).
2. Access the application whose credentials you want to renew.
3. Select Production Credentials.
4. Once there, you can renew both the Access Token and the Client Secret. To do so, click **More Options > Renew**.


> WARNING 
> 
> Important
> 
> When you renew your production credentials, you will have 12 hours during which the old credentials will remain active. It is important that you renew the credentials in your integration within this time frame.

## Share your credentials by Dashboard

If you need to share your application credentials with other Mercado Pago accounts, do so securely through **Your Applications**.
When you share your credentials, you allow another Mercado Pago account to see and use them. To do so, follow these steps:

1. Go to [Dashboard](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/panel).
2. Access the application whose credentials you want to share.
3. Click on **Share my credentials**.
4. Enter the e-mails of the Mercado Pago accounts that you want to share your credentials with. Both test and production credentials will be shared.
5. Finally, click on **Share Credentials**.

You can remove these permissions at any time from the **Credentials** panel.

> Once your integration is complete, remove any credential sharing permissions that are no longer needed to ensure privacy and security.


## Use OAuth to manage third-party credentials

OAuth is an authorization protocol that allows applications to have limited access to the private information of Mercado Pago accounts, through the HTTP protocol that introduces an authentication and authorization layer in which you request access to the protected resources of sellers, through an access token limited to a particular application, without the need for the credentials of the sellers through the access flows.

To learn more about OAuth, go to [this documentation](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/security/oauth/introduction).


> PREV_STEP_CARD_EN
>
> Best practices for your credentials
>
> Protect your data and those of the accounts you manage so that they are always safe.
>
> [Introduction](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/best-practices/safety-for-your-credentials/introduction)
