# Adicionar campos personalizados às URLs

Nota: este é um artigo de nível técnico para customização. Ajustes personalizados não são cobertos pelo suporte.

Em algumas transportadoras, não só o código de rastreio é considerado, mas outros campos também, como a Nota Fiscal, por exemplo.

Se você precisa incluir esse campo extra a cada rastreio pode fazer da seguinte maneira.

Comece incluindo o campo personalizado no plugin:

```php
add_action( 'wcasn_form_fields', 'wcasn_custom_form_fields' );  
function wcasn_custom_form_fields( $order_id ) { ?>  
  <label>Nota Fiscal</label>  
  <input type="text" name="nota_fiscal" class="wcasn-custom-fields" value="" />  
<?php }
```

Agora, dentro de cada pedido haverá uma opção para incluir o número da Nota Fiscal, e na URL do rastreio você pode inserir o campo **{nota\_fiscal}** (que é o atributo _name_ do campo criado).

Você pode incluir quantos campos quiser.

Depois, utilize o código abaixo para  substituir o {nota\_fiscal} da URL pelo valor informado no campo criado:

add\_filter( 'wc\_any\_shipping\_notify\_shipping\_company\_url', 'filter\_wcasn\_custom\_url\_fields', 20, 4 );  
function filter\_wcasn\_custom\_url\_fields( $url, $slug, $tracking\_code, $order ) {  
  if ( $custom\_url = $order->get\_meta( '\_wcasn\_' . $tracking\_code . '\_custom\_url' ) ) {  
    return $custom\_url;  
  }
  if ( isset( $\_POST\['custom\_fields'\] ) ) {  
    $find\_replace = array();  
    foreach ( $\_POST\['custom\_fields'\] as $k => $v ) {  
      $find\_replace\[ '{' . $k . '}' \] = $v;  
    }
    $url = str\_replace( array\_keys( $find\_replace ), array\_values( $find\_replace ), $url );
    $order->update\_meta\_data( '\_wcasn\_' . $tracking\_code . '\_custom\_url', $url );  
    $order->save();  
  }
  return $url;  
}

  

  

___

Keywords: