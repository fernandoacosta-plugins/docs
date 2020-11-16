# Prevenir que a tela de impressão abra automaticamente na declaração de conteúdo

Por padrão, ao clicar para imprimir a declaração de conteúdo a tela de impressão será exibida automaticamente.

Mas caso você tenha o hábito de editar as declarações antes de imprimir, pode desativar este recurso adicionando o código a seguir ao seu site:

```php
add_filter( 'wc_correios_declaration_auto_open_print_page', '__return_false' );  

```

Veja aqui como adicionar este código ao seu site: [http://ajuda.fernandoacosta.ne...](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: