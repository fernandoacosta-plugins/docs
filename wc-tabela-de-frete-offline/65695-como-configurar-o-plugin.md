# Como configurar o plugin

Neste guia há um vídeo ou opção de texto.

Faça o download do plugin acessando Minha Conta aqui no site. Instale-o normalmente pelo painel do WordPress!

Agora você já pode configurá-lo. E isso é muito simples.

Navegue até WooCommerce -> Configurações -> Entrega.

Selecione ou crie uma nova área de entrega e clique para adicionar um método de envio.

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/c38446ab-3cee-4ada-9af4-d8ea16de910a.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/c38446ab-3cee-4ada-9af4-d8ea16de910a.png)

### Configurações individuais

<span id="selection-marker-1" class="redactor-selection-marker"></span>

Agora você já pode definir os parâmetros individuais deste método específico.

-   Habilitar/desabilitar: informe se o método deve ou não ser exibido aos clientes
-   Titulo: preenchido por padrão com o nome do método importado na tabela e o prazo de entrega. Se você não irá utilizar o nome na tabela, pode defini-lo aí diretamente.
-   Dias adicionais: prazo adicional de entrega aos dias definidos na tabela
-   Unidade de medida: informe se sua tabela utiliza gramas ou kilos como unidade de peso
-   Sempre visível: se você deixar desmarcado, os métodos ficarão visíveis apenas se as outras opções falharem. Caso você esteja utilizando os Correios, por exemplo.
-   Limitar resultados: defina se quer exibir ou não múltiplos resultados para esta mesma configuração
-   Log: registre detalhes das simulações de frete para solucionar possíveis problemas.

Por fim, há a opção de importar a tabela de frete:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/bbb80ef9-bc33-4af8-b2aa-95f5a5b64753.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/bbb80ef9-bc33-4af8-b2aa-95f5a5b64753.png)

Se você não sabe como deve ser a tabela, pode baixar meu exemplo. Se você tem uma tabela em qualquer outro formato **deve** convertê-la para CSV.

Faça upload da sua tabela e a página será automaticamente atualizada. Caso contrário, clique em salvar.

Agora você poderá mapear as colunas da sua tabela para corresponderem às colunas do sistema:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/19c39f89-9edc-45de-ab5d-88d9e754d7c8.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/19c39f89-9edc-45de-ab5d-88d9e754d7c8.png)

**CEP inicial e CEP final são campos obrigatórios**.

-   CEP inicial e CEP Final: informe as colunas de faixa de CEP. Todos os CEPs que estiverem entre estes valores retornaram “verdadeiro”.
-   Peso inicial e Peso final: os pedidos **precisam** estar nesta faixa de peso para que a linha seja validada. Certifique-se de que a unidade de pedida esteja de acordo com as configurações definidas anteriormente..
-   Custo: informe a coluna referente ao custo de envio. Se nenhuma coluna for definida o frete será grátis
-   Prazo de entrega: opção com o tempo de envio. Será somado aos Dias adicionais definidos anteriormente.
-   Nome do método: opcionalmente, você pode ter um nome de método para cada linha. Se preferir, defina um nome global como mencionado acima.
-   Compra mínima para frete grátis: sempre que o valor desta coluna for menor ou igual ao pedido do cliente, ele receberá frete grátis. [Mais detalhes aqui](https://fernandoacosta.net/blog/docs/oferecer-frete-gratis-nas-compras-acima-de-r-20000/). Deixe em branco para sempre aplicar o valor da coluna “Custo”.

___

Keywords:configurar,frete offline,tabela