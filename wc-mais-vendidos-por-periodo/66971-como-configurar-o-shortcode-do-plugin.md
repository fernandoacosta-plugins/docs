# Como configurar o shortcode do plugin

Para exibir os produtos mais vendidos por período você deve usar o shortcode:

```php
[best_selling_by_period]
```

Isso vai exibir os produtos mais vendidos dentro da configuração padrão, que são:

-   Total de 12 produtos
-   Em 4 colunas (3 de linhas com 4 produtos em cada)
-   Nos últimos 7 dias.

## Intervalos customizados

Você pode customizar o shortcode adicionando outros parâmetros. O mais importante é "period", por exemplo:

\[best\_selling\_by\_period period="year"\]

Irá exibir os 12 produtos mais vendidos (padrão, ver abaixo como modificar) desde o dia 1 de janeiro do ano atual até o presente.

As opções padrão são:

-   **7day**: exibe os mais vendidos dos últimos 7 dias
-   **month:** mais vendidos desde o dia 01 do mês atual até agora
-   **last\_month**: mais vendidos no mês passado
-   **year**: desde o dia 1 de janeiro do ano atual até o presente
-   **custom**: intervalo de dias personalizados (ver mais detalhes abaixo)

Trabalhando com intervalos personalizados

Se você pretende exibir o shortcode para datas fixas, como, por exemplo, de 01 de março até 15 de março, você deve usar o valor **custom** para o atributo **period**. Ficando period="custom".

Além disso, você deve informar as datas de início (start\_date="") e fim (end\_date=""). No exemplo citado, o shortcode ficará assim:

\[best\_selling\_by\_period period="custom" start\_date="2018-03-01" end\_date="2018-03-15"\]

Repare que o formato da data é **AAA-MM-DD**. 

O atributo **start\_date** é obrigatório. Se o atributo **end\_date** estiver faltando, será usando o dia atual.

## Customizando o número de colunas

Por padrão, são exibidas 4 colunas. Se você quer mudar isso, basta usar o atributo **columns**, como exemplo abaixo:

\[best\_selling\_by\_period columns="3"\]

Modificando o total de produtos

O padrão são os 12 produtos mais vendidos dentro do período selecionado, para modificar utilize o atributo **limit**.

\[best\_selling\_by\_period limit="4"\]

  

___

Keywords:mais vendidos,configurar mais vendidos,mais populares