# Mantenha suas credenciais seguras

Ao integrar as soluções do Mercado Pago, você lidará com dados confidenciais que deve proteger de possíveis perdas ou vulnerabilidades. Esses dados podem ser suas credenciais, as de suas integrações e as de seus clientes.

Credenciais são senhas exclusivas com as quais identificamos uma integração em sua conta. Elas são usadas ​​para capturar pagamentos em lojas online e outras aplicações de forma segura. Para obter informações detalhadas sobre as credenciais, acesse [Credenciais](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/resources/credentials).

Mostraremos como você pode otimizar a segurança de suas integrações de forma simples e rápida.

## Envie o access token por header

Sempre que você fizer chamadas de API, **envie o Access Token via header** em vez de via query param. Isso permitirá que você proteja seu Access Token de ser exposto a qualquer pessoa fora de sua integração.

Por exemplo, se você fizer um GET para o endpoint _/users/me_, ficaria assim:

```curl
curl -H 'Authorization: Bearer APP_USR-12345678-031820-X-12345678' \
https://api.mercadolibre.com/users/me
```
Sempre mantenha suas credenciais ocultas e não as exponha em nenhum parâmetro ou no lado público de sua integração.

## Renove suas credenciais periodicamente

Recomendamos que você renove suas credenciais com frequência para evitar possíveis vulnerabilidades.

Renove suas credenciais de maneira simples seguindo estas etapas:

1. Acesse [Dashboard](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/panel).
2. Acesse a aplicação cujas credenciais você deseja renovar.
3. Selecione as Credenciais de produção.
4. Uma vez lá, você pode renovar o Access Token e o Client Secret. Para fazer isso, clique em **Mais opções > Renovar**.


> WARNING 
> 
> Importante
> 
> Ao renovar suas credenciais de produção, você terá 12 horas durante as quais as credenciais antigas permanecerão ativas. É importante que você renove as credenciais em sua integração dentro desse prazo.

## Compartilhe suas credenciais pelo Dashboard

Se você precisar compartilhar as credenciais da sua aplicação com outras contas do Mercado Pago, faça isso de forma segura por meio de Suas Aplicações.
Ao compartilhar suas credenciais, você permite que outra conta do Mercado Pago as veja e use. Para fazer isso, siga estas etapas:

1. Acesse [Dashboard](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/panel).
2. Acesse a aplicação cujas credenciais você deseja compartilhar.
3. Clique em **Compartilhar minhas credenciais**.
4. Insira os e-mails das contas do Mercado Pago com as quais deseja compartilhar suas credenciais. Tanto o teste quanto a produção serão compartilhados.
5. Por fim, clique em **Compartilhar credenciais**.

Você pode remover essas permissões a qualquer momento no painel Credenciais.

Assim que a integração for concluída, remova quaisquer permissões de compartilhamento de credenciais que não sejam mais necessárias para garantir privacidade e segurança.

## Utilize o OAuth para gerenciar credenciais de terceiros

OAuth é um protocolo de autorização que permite que aplicativos tenham acesso limitado às informações privadas das contas do Mercado Pago, por meio do protocolo HTTP que introduz uma camada de autenticação e autorização na qual você solicita acesso aos recursos protegidos dos vendedores, por meio de um token de acesso limitado a um determinado aplicativo, sem a necessidade das credenciais dos vendedores através dos fluxos de acesso.

Para saber mais sobre o OAuth, acesse [esta documentação](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/security/oauth/introduction).

> PREV_STEP_CARD_PT
>
> Boas práticas de segurança para suas credenciais
>
> Proteja seus dados e os das contas que você gerencia para que estejam sempre seguros.
>
>[Introdução](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/best-practices/safety-for-your-credentials/introduction)