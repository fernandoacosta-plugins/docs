# Dados de acesso para integrar ao plugin

Para usar o plugin WC Correios Status Updater é necessário ter contrato com os Correios. Os dados de acesso não são do SIGEP web, mas sim login e senha **exclusivos para o webservice de rastreamento de objetos**.  

Se você já tem o contrato, deve solicitar ao seu gerente de conta dos Correios os dados de acesso ao **webservice de rastreamento de objetos**. Informe que você está fazendo integração com seu sistema.

A maior das pessoas não possuem esse login e senha por padrão, sendo necessário solicitá-lo diretamente ao gerente dos Correios.

Os dados são enviados por e-mail e podem demorar um pouco.

## Recebi os dados mas ainda não funciona

Nesse caso, infelizmente os dados estão errados. Se você continua vendo a mensagem de que os dados são inválidos, quer dizer que são, já que a mensagem é retornada diretamente do Webservice de rastreamento dos Correios (SRO). Você pode tentar entrar em contato com seu gerente dizendo que os dados não funciona e que o webservice que você está tentando acessar é este: ```php
https://webservice.correios.com.br/service/rastro/Rastro.wsdl
```

___

Keywords:correios,login,senha,webservice,rastreamento de objetos,sigep