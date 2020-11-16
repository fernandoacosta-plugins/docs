# Como enviar links encurtados no WhatsApp

Alguns boletos geram umas URLs gigantes e feias. Se você quer encurtá-las no plugin WhatsApp agora é possível com o pequeno código abaixo.

Ele é integrado com o bit.ly e você precisa pegar o seu [token aqui](https://support.bitly.com/hc/en-us/articles/230647907-How-do-I-find-my-OAuth-access-token-).

Depois adicione o código abaixo ao seu site. Não esqueça de mudar onde diz **SEU\_TOKEN** pelo token obtido na sua conta do Bit.ly, é grátis!

```php
function fa_wc_whatsapp_short_link( $args, $order ) { $bitly_token = 'SEU_TOKEN'; if ( isset( $args['payment_url'] ) ) { if ( $custom_url = $order->get_meta( '_wc_whatsapp_custom_url_v2' ) ) { $args['payment_url'] = $custom_url; } else { $response = wp_remote_get( 'https://api-ssl.bitly.com/v3/shorten?access_token=' . $bitly_token .'&format=txt&longUrl=' . urlencode( $args['payment_url'] ) ); if ( ! is_wp_error( $response ) && 200 === wp_remote_retrieve_response_code( $response ) ) { $args['payment_url'] = $response['body']; $order->update_meta_data( '_wc_whatsapp_custom_url_v2', $response['body'] ); $order->save(); } } } return $args; } add_filter( 'wc_whatsapp_pending_orders_payment_data', 'fa_wc_whatsapp_short_link', 10, 2 ); add_filter( 'wc_whatsapp_pending_orders_get_payment_data', 'fa_wc_whatsapp_short_link', 10, 2 );
```

___

Keywords: