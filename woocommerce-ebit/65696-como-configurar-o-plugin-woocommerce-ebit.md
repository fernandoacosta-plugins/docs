# Como configurar o plugin WooCommerce Ebit

As configurações do plugin estão disponíveis em WooCommerce -> Configurações -> Integração -> Ebit.

### Entendendo os campos

**ID da Loja**: é o identificador único da sua loja no Ebit. Normalmente fica dentro do seu painel. Se não encontrar, é necessário solicitar ao atendimento do Ebit.

**Prioridade**: o banner é exibido automaticamente no checkout. A prioridade coloca ele mais pra cima ou pra baixo na tela. Para testar você pode criar um pedido e, no checkout, ir mudando a prioridade e atualizando a página até chegar a posição que deseja exibí-lo. Quanto mais alto o número, mais para baixo o banner ficará.  

**Banner por e-mail**: se você informar a URL de uma imagem o banner do Ebit também será exibido nos e-mails do WooCommerce que forem enviados até 24h depois da compra ser realizada.  

Para o banner do checkout não é necessário informar uma URL porque ele é fornecido pelo sistema do Ebit. Já para o banner do e-mail você deve criar um banner do zero, **seguindo as recomendações do Ebit**.

Depois de criar o banner, você deve enviá-lo ao Ebit para aprovação e só então você estará autorizado a utilizá-lo. Por isso **não configure o banner no plugin até receber esta autorização**. O manual de boas práticas do banner por e-mail deve ser solicitado diretamente ao Ebit.

Depois de configurado, você pode testar a integração [clicando aqui](https://www.ebit.com.br/developer/validar-integracao). Note que:

-   Só é possível testar **depois de receber pedidos** e o banner ser exibido
-   Pode demorar até 120 minutos para que o pedido apareça no Ebit.

Além do banner no checkout você pode exibir uma medalha do Ebit no seu site. Para isso, basta ir até Painel -> Aparência -> Widgets -> Incluir um widget de texto onde pretende exibir a medalha (geralmente no rodapé) e escrever o seguinte nele:

\[wc\_ebit\_medalha\]

Automaticamente o plugin irá converter este shortcode na medalha do Ebit.

**Importante!**

Apenas o campo ID da Loja no Ebit é obrigatório. Com isso o banner e o lightbox Ebit serão automaticamente exibidos na página de obrigado da sua loja. O banner no e-mail é totalmente opcional.

___

Keywords:ebit,woocommerce ebit,configurações