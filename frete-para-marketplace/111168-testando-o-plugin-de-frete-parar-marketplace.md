# Testando o plugin de frete parar marketplace

Primeiro de tudo, certifique-se de que a versão que você tem instalada é a 1.1.1 ou superior.

Feito isso, vamos às configurações.

**PAC e SEDEX não aparecem**

A forma mais simples de testar isso é desativando o plugin de frete para marketplace. Dessa forma, apenas o plugin WooCommerce Correios estará funcionando. Os métodos de envio **precisam aparecer**, só que a restrição aqui é que ele sempre será calculado com o CEP da Loja, e não dos vendedores.

Os problemas mais comuns são:

\- Você não preencheu o peso do produto (Revise isso! Não esqueça que o limite é 30 kg)

\- Você  não preencheu as dimensões do produto

\- Valor declarado. No caso do SEDEX o mínimo é R$ 20,50. Então se seu produto é mais barato que isso, não funciona. Desative essa opção.

As duas informações são obrigatórios nos Correios. Não é uma exigência dos plugins,  mas dos Correios.

\----

Os métodos aparecem, mas quando ativo o plugin eles somem.

Isso acontece porque o CEP do vendedor não está cadastrado ou é inválido.

Certifique-se  de que essas informações estejam corretas.  Caso sim, faça o procedimento a seguir:

\- Vá até WooCommerce -> Status -> Logs -> exclua todos os logs que comecem com **correios-sedex**...

Depois, vá até  WooCommerce -> Configurações -> Entrega -> Edite a área de entrega e então o método SEDEX e ative os logs deste método.

Agora, vá até o carrinho do seu site e faça uma simulação. Somente assim os logs serão registrados.

Navegue até WooCommerce -> Status -> Logs, procure por um log que comece com correios-sedex e me envie que irei analisar e auxiliar.

___

Keywords: