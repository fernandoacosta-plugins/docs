# Restringir o envio de alguns e-mails a clientes

Por padrão, todas as atualizações de status são enviadas aos clientes. Você pode utilizar o filtro ```php
wc_correios_status_updater_notification_status_not_allowed
``` para prevenir o envio de alguns e-mails, como aquele de “Objeto ainda não chegou a unidade”.  

add\_filter( 'wc\_correios\_status\_updater\_notification\_status\_not\_allowed', 'wc\_correios\_prevent\_email\_notification', 10 );  
function wc\_correios\_prevent\_email\_notification( $statuses ) {  
  $statuses\[\] = 69;  
    
  return $statuses;  
}

[Ver no Gist](http://gist.github.com/fernandoacosta/015ae902f92e0418e71e7b44c3f264d8#file-functions-php).

\*Esta mensagem pode aparecer em diversos status, mas o 69 é o mais comum\*.

Você deve personalizar este código da forma que for mais útil a você com base nos status disponíveis na documentação dos Correios.

Os Correios disponibilizam uma lista de eventos que pode ser consultada aqui -> [https://www.correios.com.br/en...](https://www.correios.com.br/enviar-e-receber/precisa-de-ajuda/lista-de-eventos-rastreamento-de-objetos)

___

Keywords:correios,emails,restringir e-mails,notificações