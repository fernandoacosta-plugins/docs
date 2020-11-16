# Como remover o "destino" de entrega do carrinho

Desde a versão 3.5.0 o WooCommerce exibe na página do carrinho uma mensagem informando que a estimativa de entrega é para determinado endereço.

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/057d8d8a-ca83-4c6f-aba2-3747ae57620f.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/057d8d8a-ca83-4c6f-aba2-3747ae57620f.jpg)

No entanto, isso só vai funcionar adequadamente se o cliente preencher cidade, estado e CEP na calculadora de frete.

O que não faz nenhum sentido, já que podemos calcular o frete apenas com o CEP. E só usamos o Estado para definir áreas de entrega no WooCommerce - que não podem ser definidas por nome da cidade.

O campo CEP fica preenchido, indicando que a cotação é para aquele endereço.

O plugin Otimização da Calculadora de Frete na página do Carrinho identifica automaticamente o estado a partir do CEP, mas identificar a cidade não é possível\*, então os dados da estimativa podem ficar inconsistentes.

Sendo assim, o ideal é remover essa informação do carrinho - ou exigir que o cliente preencha cidade e estado também, o que não faz sentido mais uma vez.

Para ocultar essa informação, basta ir até WooCommerce -> Configurações -> Entrega -> Opções de envio e marque a opção "Ocultar estimativa".

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/a8b12ffe-cff0-424a-95b9-286a6b619174.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/a8b12ffe-cff0-424a-95b9-286a6b619174.jpg)

  

\*Até dá, mas seria necessário comprar a base de CEP dos Correios que custa cerca de R$ 2500 + R$ 800 a cada três meses para renovação.

___

Keywords: