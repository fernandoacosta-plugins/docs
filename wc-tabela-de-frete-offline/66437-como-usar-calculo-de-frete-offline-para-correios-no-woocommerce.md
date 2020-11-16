# Como usar cálculo de frete offline para Correios no WooCommerce

Pela facilidade de uso e por estarem em praticamente todas as cidades do país, os Correios acabam se tornando uma opção muito atrativa a muitos e-commerces, especialmente aqueles que estão começando e não possuem uma demanda grande o bastante para contratar uma transportadora - ou, às vezes, preferem os Correios.  

O grande problema é que com bastante frequência o webservice dos Correios, sistema de consulta consulta de dados em tempo real, fica indisponível. Com isso, as lojas que não estão preparadas acabam ficando sem nenhuma opção de entrega disponível. O cliente não conseguirá finalizar a compra e, quase certo, irá buscar outro fornecedor. Caso a sua loja com WooCommerce tenha algum problema de ajuste, pode acontecer, ainda, do cliente conseguir finalizar a compra mesmo sem calcular o frete -- o que pode representar um prejuízo se forem muitos pedidos.

Além destes problemas mais evidentes, há também a experiência da compra do usuário. Porque parece que a loja não é profissional o bastante ou que não atende na região do consumidor, já que a mensagem padrão não é genérica e não informa que trata-se de um problema temporário.

Uma solução para este problema é uma tabela de fretes offline com os **dados reais dos Correios**.

## Configurar frete offline

Aqui vamos ver um passo a passo de como configurar uma tabela offline na sua loja com WooCommerce. Dessa forma, a consulta será local, dentro do seu próprio servidor. Com isso, há dois benefícios evidentes:

-   Velocidade de carregamento: a checagem de preços e prazos é feita rapidamente dentro do seu próprio servidor
-   Disponibilidade: você não dependerá mais do webservice dos Correios -- pelo menos não o tempo todo. Nas consultas diárias feitas por clientes ele não será necessário, somente quando você decidir atualizar a tabela de preços para garantir que todos os valores e prazos estão de acordo.

### Gerar tabelas de frete

Para os clientes que possuem uma licença ativa do plugin **Frete Offline com Tabela para WooCommerce** é possível gerar a tabela gratuitamente e de forma simplificada.

Acesse o site: [http://apps.fernandoacosta.net](http://apps.fernandoacosta.net/)

Informe seu CEP de origem e, se for o caso, os dados de contrato com os Correios.

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/959816f7-fa70-4017-accc-ff43dd5039ad.jpg)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/959816f7-fa70-4017-accc-ff43dd5039ad.jpg)

Você deve gerar duas planilhas: uma para PAC e outra para SEDEX. Feito isso, você já terá todos os dados que gerados pelos Correios salvos no seu computador.  

### Integrando com seu site

Utilizando o plugin [**Frete Offline com Tabela para WooCommerce**](https://fernandoacosta.net/produto/frete-tabela-offline/) você pode importá-las no seu site para poder calcular o frete offline.

Basta acessar WooCommerce -> Configurações -> Entrega -> escolher uma área de entrega e adicionar um novo método:

![](https://fernandoacosta.net/wp-content/uploads/2018/04/anim.gif)

Dentro do plugin você pode mapear todas as colunas para que funcionem perfeitamente no seu site:

![](https://fernandoacosta.net/wp-content/uploads/2018/04/02.png)

Está pronto! Agora você pode até mesmo desabilitar o plugin WooCommerce Correios. A minha recomendação é que você desabilite os métodos de envio, mas mantenha o plugin ativo. Dessa forma o seu site continuará com o excelente recurso de auto completar endereço e também de informar códigos de rastreio para cada pedido.

A configuração é bastante simples e foi rápida. Com ela você vai com certeza salvar várias vendas e aumentar a velocidade do seu carrinho e checkout.

Deixe seu comentário caso tenha alguma dúvida.

___

Keywords:correios,offline,tabela de frete,frete offiline,frete ĺocal