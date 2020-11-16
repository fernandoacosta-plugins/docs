# Métodos de entrega não aparecem

Se você está enfrentando problemas ao exibir os métodos de entrega, verifique alguns pontos mais comuns.

## Verificar áreas de entrega

Certifique-se de que os métodos offline estão dentro da área de entrega selecionada. O WooCommerce irá verificar as áreas de entrega **de cima para baixo**.

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/1a674dc0-9f8f-4f8f-ac7e-8d82a5781a0a.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/1a674dc0-9f8f-4f8f-ac7e-8d82a5781a0a.jpg)

Na imagem acima,  há duas áreas de entrega para **Brasil**. Na primeira, há apenas PAC. Na segunda, há o método offline. A primeira é válida, então as demais serão ignoradas.

Então verifique se suas áreas de entrega não estão sendo sobrepostas.

## Verificar mapeamento da tabela

Se está tudo certo com suas áreas de entrega, verifique se o método offline foi mapeado corretamente.

Após fazer upload de uma tabela offline você deve mapeá-la para que o plugin saiba qual campo contem cada informação (CEPs, peso etc).

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/d7af03e9-f6ee-4641-a538-856c395f9279.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/d7af03e9-f6ee-4641-a538-856c395f9279.jpg)

Certifique-se de que cada campo tem um valor único e adequado.

## Verificar faixas de peso e CEP

Na imagem acima você pode ver o link **nova-tabela.txt**, que é o nome do seu arquivo. Clique nele.

Você irá ver toda a tabela. Certifique-se de que o peso do carrinho está contido em uma faixa de peso da tabela.

Faça o mesmo com a faixa de CEPs. O CEP do cliente no carrinho está contido em alguma linha da tabela?

Se sim, verifique os dois casos. Em uma **mesma linha** você precisa ter CEP e peso do carrinho válidos. Somente assim o método será exibido, com a validação de CEP e peso.

## Continua com problemas?

Posso ajudar! Me envie as imagens de cada etapa citada aqui e o link da tabela. Bem como peso dos produtos do carrinho e CEP que está tentando validar.

___

Keywords: