# Obtener datos de la tienda

Para obtener información sobre todas las tiendas que están vinculadas a **un usuario específico**, realice un GET enviando el `user_id` y el `access-token` (generados por el proceso de autenticación de OAuth) al punto final [[/proximity-integration/users/{seller_id}/stores](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/reference/mp_delivery/_proximity-integration_users_seller_id_stores/get). Consulte [Seguridad](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/guides/security/oauth/introduction) para obtener más información sobre OAuth.

También es posible consultar información de una **tienda específica** usando su **ID**. Para ello, realiza un GET enviando el `store_id` y el `access-token` al endpoint [/proximity-integration/stores/{StoreID}](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/reference/mp_delivery/_proximity-integration_stores_store_id/get).

Este punto de enlace devuelve todos los datos del punto de enlace anterior, además de información sobre el estado actual del almacenamiento ("habilitado", "en pausa" o "deshabilitado"). Consulta [Cambiar estado de tienda](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/guides/mp-delivery/print-order-receipt) para obtener más información sobre los estados.

> NOTE
>
> Importante
>
> También podrás consultar la información de una tienda a través de su ID externo, si lo tiene. Para eso, envíe como parámetros de solicitud el `user_id` relacionado con la tienda, el `external_id` y el `access_token`. Vea más información en la API [Obtener tienda por ID externo](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/reference/mp_delivery/_proximity-integration_users_SellerID_stores_external_id_ExternalID/get).
> </br>
> Para saber cómo crear un ID externo para tu tienda y utilizarlo como identificador para el sistema de software de gestión de pedidos, accede a [Cambiar ID externo de la tienda](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/reference/mp_delivery/change-store-external-id)

> NEXT_STEP_CARD_ES
>
> Cambiar el estado de la tienda
>
> Aprenda a cambiar el estado de funcionamiento de la tienda de la tienda.
>
> [Cambiar estado de tienda](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/guias/mp-delivery/change-store-status)