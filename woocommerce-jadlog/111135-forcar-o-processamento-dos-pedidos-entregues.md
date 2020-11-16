# Forçar o processamento dos pedidos entregues

Em algumas raras ocasiões, pode ser que o seu site trave bem no meio do processamento da verificação de quais pacotes foram entregues para atualizar o status.

Isso pode acontecer por alguns motivos.

Embora o plugin tente controlar isso, pode acontecer se a JadLog estiver fora do ar.

Se o cron do seu site for desligado etc.

Eventos pouco comuns, mas possíveis.

Isso faz com que a fila fique com o status "Em andamento", mas travada.

Desde a versão 1.2.0 é possível resolver isso indo até WooCommerce -> Status -> Ferramentas -> e buscando por **Executar cron JadLog**. Execute o evento e pronto.

Ao fazer isso, sempre será registrado um log chamado "jadlog-force-execution", que vai informar se a fila estava realmente travada ou não.

Ainda que o objetivo seja corrigir este problema pontual, você pode usar este recurso para executar a fila a qualquer momento, sob demanda.

___

Keywords: