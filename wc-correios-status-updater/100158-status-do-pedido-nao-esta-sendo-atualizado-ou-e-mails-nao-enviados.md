# Status do pedido não está sendo atualizado ou e-mails não enviados

O plugin é feito para atualizar automaticamente os pedidos depois de ser entregue e também notificar ao cliente sempre que houver uma mudança no status da entrega.

Se isso não está acontecendo, verifique o seguinte:

-   Em WooCommerce -> Configurações -> Correios Updater o status para atualizar o pedido está definido? **Se não, defina**.
-   Ainda nas configurações, é exibida a mensagem de sucesso para o rastreio teste? [Se não, verifique o login e senha](http://ajuda.fernandoacosta.net/article/show/65719-dados-de-acesso-para-integrar-ao-plugin).
-   Em WooCommerce -> Configurações -> E-mails -> está ativo o e-mail **Andamento da entrega dos Correios**? Se não, ative-o se quiser que o cliente seja notificado
-   Verifique o cron seguindo o passo a passo abaixo.

1\. Instale o plugin WP Crontrol. Vá até seu painel -> Plugins -> Adicionar Novo e procure por WP Crontrol. Instale e ative.

2\. Vá até Ferramentas -> Eventos Cron.

3\. Procure o evento wc\_correios\_status\_updater\_cron.

4\. Não encontrou? No final da página, crie-o conforme a imagem abaixo:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/68a48feb-98ff-4749-a682-4862e66007d1.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/68a48feb-98ff-4749-a682-4862e66007d1.jpg)

Atualize a página. O evento deve ser exibido como na imagem abaixo, com execução para "Agora".

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/da04dc59-02af-4936-8d36-541fcb379e7b.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/da04dc59-02af-4936-8d36-541fcb379e7b.jpg)

[](https://d29l98y0pmei9d.cloudfront.net/article/2624/35cbbd75-4158-4b74-8544-4755e2aa6b72.jpg)

Aguarde cerca de 2 minutos e atualize a página.

Verifique se o total de pedidos pendentes de atualização diminuiu.

**Está vendo muitos eventos cron com execução indicando AGORA**? Isso quer dizer que a fila de crons do seu site não funciona. Verifique com a hospedagem ou seu desenvolver como resolver.  

O **cron existe e mesmo assim o status não é atualizado**? Volte às configurações do plugin e ative o log.

Feito isso, vá até o painel do WP Crontrol, procure o evento wc\_correios\_status\_updater\_cron e clique em **executar agora**.

Aguarde 5 minutos.

Vá até WooCommerce -> Status -> Log -> procure por correios\_updater (algo assim) e envie os detalhes no e-mail suporte@fernandoacosta.net

___

Keywords: