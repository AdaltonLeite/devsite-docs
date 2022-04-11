# Get order data

To query data from an order, perform a GET sending the `shipment_id` and `access-token` (generated by the OAuth authentication process) to the endpoint [/proximity-integration/v1/orders/{shipmentId}](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/reference/mp_delivery/_proximity-integrationorders_shipment_id/get). See [Security](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/security/oauth/introduction) for more information about OAuth.

* **Merchant**: information about the restaurant that received the order.
* **Items**: description of the items and additional items in the order.
* **OtherFees**: shipping and transaction fee information.
* **Discounts**: discounts applied to the order.
* **Total**: total amount paid on an order.
* **Payments**: information about the payment method for an order.
* **Customer**: data about the buyer.
* **Delivery**: information about the delivery location.
* **Extension.status**: current status of the order.
  * **Pending**: initial status of the order. It means that the order is being created and will be handled later.
  * **Handling**: the order is being assembled and waiting for a response from the system, such as the completion of payment by the customer.
  * **Ready_to_ship**: this status has two substatus that denote that an order is deliverable (because it has been received and can be accepted or because it has been accepted and can be printed).
  * **Shipped**: order on the way.
  * **Not_delivered**: order wasn't delivered.
  * **Delivered**: order delivered.
  * **Cancelled**: order canceled.
  <br/>
* **Extension.substatus**: substatus in which the order is. The substate relates directly to the state.
  * **Pending > creating_route**: order route being created.
  * **Handling > null**: will indicate the reason why the order is waiting for its acceptance.
  * **Ready_to_ship > ready_to_print**: waiting for order acceptance.
  * **Ready_to_ship > printed**: order accepted and printed.
  * **Out_for_delivery**: order went out for delivery. 
  * **Delivery_failed**: delivery not completed.

> PREV_STEP_CARD_EN
>
> Order management
>
> Learn how to manage orders with Mercado Pago Delivery.
>
> [Order management](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/mp-delivery/order-management)

> NEXT_STEP_CARD_EN
>
> Accept order
>
> Learn how to accept orders with Mercado Pago Delivery.
>
>[Accept order](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/mp-delivery/accept-order)