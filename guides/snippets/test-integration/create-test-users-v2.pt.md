As contas de testes são necessárias para verificar se o processo de integração ocorreu corretamente. Elas têm os mesmos recursos de uma conta real do Mercado Pago, o que permite testar o funcionamento das integrações que você está desenvolvendo.

Para realizar teste é preciso ter pelo menos duas contas:

* Usuário/Vendedor: conta necessária para **configurar a aplicação e as credenciais para a cobrança**. Esta é a sua conta de usuário.
* Comprador: conta necessária para **testar o processo de compra**.

Além dessas contas, é importante também utilizar os [cartões de teste](/developers/pt/guides/additional-content/testing/test-cards) para testar a integração de pagamento e simular o processo de compra, assim como o saldo na conta do Mercado Pago do usuário de teste. Veja mais detalhes abaixo.

Para criar contas e testar o funcionamento das integrações, siga os passos abaixo.

1. No Devsite, acesse o menu **Suas integrações > Contas de teste** e clique no botão **Criar contas teste**.
2. Na tela "Criar nova Conta", insira uma descrição para identificação da conta. Exemplo: "Vendedor loja 1".
3. Em seguida, selecione o **país de operação** da conta. Essa informação não poderá ser editada posteriormente e, além disso, os usuários Comprador e Vendedor precisam ser do mesmo país.
4. Preencha com um **valor fictício em dinheiro** que servirá como referência para você testar suas aplicações. Esse valor aparecerá como saldo na conta do Mercado Pago do usuário de teste e poderá ser utilizado para simulação de pagamentos, assim como com cartão de crédito.
5. Clique em **Criar conta de teste**. 

> Você pode gerar até 15 contas de usuários de teste ao mesmo tempo e, por enquanto, ainda não é possível deletá-las.

Pronto! A conta de teste foi criada e será exibida na tabela com as seguintes informações:

![testuser](test-user/test-user-admin-1.png)
![testuser](test-user/test-user-admin-2.png)
![testuser](test-user/test-user-admin-3.png)
![testuser](test-user/test-user-admin-4.png)
![testuser](test-user/test-user-admin-5.png)
![testuser](test-user/test-user-admin-6.png)
![testuser](test-user/test-user-admin-7.png)
![testuser](test-user/test-user-admin-8.png)
![testuser](test-user/test-user-admin-9.png)
![testuser](test-user/test-user-admin-10.png)

* **País** local de origem da conta selecionado em seu cadastro.
* **Identificação da conta**: descrição para identificação da conta de teste.
* **Usuário**: username da conta de teste gerado automaticamente. Esse username é utilizado para se fazer login com o test user.
* **Senha**: senha de acesso à conta do usuário de teste gerada automaticamente. Para gerar uma nova senha, clique nos 3 pontos verticais ao final da linha da tabela e selecione a opção **Gerar nova senha**.
* **Data de criação**: data em que a conta de teste foi criada. 

> NOTE
>
> Importante
>
> Para editar a **identificação da conta** ou **adicionar mais valor fictício em dinheiro** para testar suas aplicações, clique nos 3 pontos verticais e selecione a opção **Editar dados**. <br>