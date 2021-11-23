# Configurar condições de pagamento

**Condições de pagamento** são as formas de pagamento exibidas no site para a finalização de compra. Permitem a configuração de parcelamento, juros, condições especiais etc.

Após ter criado sua afiliação com o **MercadoPagoV2**, você deverá configurar as **condições de pagamento** que serão oferecidas aos compradores.

> WARNING
>
> Importante
>
> Certifique em sua loja de aplicativos da VTEX se o App **Mercado Pago Payment APP** está instalado para utilização das condições de pagamento **MercadoPagoPro, MercadoPagoWallet e MercadoPagoOff** ou solicite a instalação para a equipe de VTEX através do [Support VTEX](https://help.vtex.com/es/support).

A configuração das condições de pagamento é feita na aba **Condições de pagamento** do menu **Configurações** no módulo de **Pagamentos** no portal do administrador da plataforma VTEX.  Nessa aba, você deverá clicar no botão  "+" (*Adicionar nova condição de pagamento para...*) e selecionar uma das seguintes condições de pagamento:

* **Cartão de Crédito:** refere-se a transações com cartões de crédito diretamente no site da sua loja. Este configuração requer que você selecione cada bandeira de cartão de crédito que deseja em sua loja. [Você pode clicar aqui para descobrir quais bandeiras de cartão de crédito você pode selecionar](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/plugins/unofficial/vtex/payment-methods). Além disso, sua configuração pode exigir o preenchimento de campos adicionais dependendo das condições de pagamento que selecionar (À vista ou Parcelado). Para mais informações sobre como configurar parcelas na VTEX, clique [aqui](https://help.vtex.com/pt/tutorial/condicoes-de-pagamento--tutorials_455#parcelado-sem-juros). ----[mla, mlu, mlc, mlm, mpe, mco]----
* **Cartão de Débito:** refere-se a transações com cartões de Débito. ------------
* **Outro:** refere-se à transações com **MercadoPagoOff**, **MercadoPagoWallet**, ou **MercadoPagoPro**.
  * Se você configurar **MercadoPagoPro**, o comprador realizará o pagamento no ambiente do Mercado Pago, via formulário apresentado diretamente em sua loja e terá acesso a todos os meios de pagamentos disponíveis da plataforma.
  * Se você configurar **MercadoPagoWallet**, o comprador utilizará sua carteira do Mercado Pago. Este modo é exclusivo para compradores cadastrados no Mercado Pago ou Mercado Livre e sugerimos utilizar caso opte pela **Condição de Pagamento Cartão de Crédito**.
  * Se você configurar **MercadoPagoOff**, poderá contar com os meios de pagamento em dinheiro, como por exemplo, Boleto Bancário e PEC (pagamentos em lotéricas).----[mlb]----
* **Boleto Bancário:** refere-se a transações com boleto bancário **exclusivamente**.
* **Pix:** refere-se a transações com Pix através de **QR Code** ou de **Copia e Cola**. Para configurar esta condição de pagamento é necessário que tenha uma chave Pix cadastrada na sua conta do Mercado Pago. Para obter mais informações sobre como criar sua chave Pix, clique [aqui](https://www.mercadopago[FAKER][URL][DOMAIN]/stop/pix?url=https%3A%2F%2Fwww.mercadopago.com.br%2Fadmin-pix-keys%2Fmy-keys&authentication_mode=required). ------------

> NOTE
>
> Nota
> 
> Você também pode configurar **condições especiais** de pagamento. Clique [aqui](https://help.vtex.com/pt/tutorial/condicoes-especiais--tutorials_456?&utm_source=admin) para obter mais informações.

![Configurar condições de pagamento](/images/vtex/paymentconditions-pt.gif)

Na próxima tela, deve-se:

1. Escrever o **Nome da Regra**.  Você pode escrever qualquer nome para identificá-la facilmente.
2. Selecionar **MercadoPagoV2** na lista oferecida pelo campo `Processar com a afiliação`.
3. Ativar a condição de pagamento no campo `Status`. Ele deve estar ativado para que sua seleção no campo `Processar com a afiliação` funcione.
4. Salvar suas alterações clicando em `Salvar`.

![Configurar condições de pagamento com cartão de crédito](/images/vtex/paymentconditions-cc-pt.gif)

> WARNING
>
> Importante
> 
> As mudanças nas Condições de pagamento podem levar até 10 minutos para serem aplicadas.

Para mais informações sobre como configurar as condições de pagamento na VTEX, clique [aqui](https://help.vtex.com/pt/tutorial/condicoes-de-pagamento--tutorials_455).

> NOTE
>
> Nota
> 
> Se você tiver dificuldades durante sua integração, verifique nosso [lista de erros](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/plugins/unofficial/vtex/common-errors) e nosso documento sobre [logs do VTEX](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/plugins/unofficial/vtex/logs).


> LEFT_BUTTON_REQUIRED_PT
>
> Device Fingerprint
>
> Conheça como configurar o fingerprint.
>
> [Device Fingerprint](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/plugins/unofficial/vtex/device-fingerprint)