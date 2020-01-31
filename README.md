# SOBRE O PROJETO
  Esse projeto visa ajudar cidades pequenas a se comunicar com seus habitantes. Cidades grandes e mais estruturadas têem comunicação em massa e mídia ativa bem ampla, porém, cidades pequenas carecem de credibilidade e amplitude nas comunicações.
 
  O projeto nasceu apartir do desastre causado nas cidades do Sudeste após as chuvas no Leste do estado de Minas, especialmente na cidade de Espera Feliz, uma pequena e pacata cidade de 25 mil habitantes. Cujo qual, os governantes as 18:00 saberiam que haveria uma enchente, porém não conseguiram avisar a população de forma efetiva, e, por volta das 04:00 da manhã, 75% da cidade foi coberta por lama e caos.
  
  Por sorte, dessa vez, não houve óbitos, porém, precaver é necessário, então esse projeto vem no intuito de dar credibilidade e amplitude na comunicação das prefeituras de pequenas cidades com seus moradores.

## VISÃO GERAL
  O projeto deverá ser separado em microsserviços, cada um com seu container próprio, sua tecnologia própria, completamente independente um do outro, devem se comunicar via REST-API. Os containers podem, e devem, ser hospedados em estados serverless, utilizando o HEROKU gratis. - talvez no futuro possamos utilizar o AWS -
  
### MICROSSERVIÇOS
Em breve irei criar nesse mesmo perfil um repositório para cada microsserviço listado abaixo, com um readme específico e uma lista de FEATURES.
- Admin Panel:
  + Painel administrativo, esse microsserviço deve ser desenvolvido com REACT ou ANGULAR, apenas front-end consumindo API's, não haverá backend nesse serviço.
  + O painel servirá para o administrador municipal do serviço visualizar a taxa de entrega das mensagens, taxa de abertura, quantas mensagens foram enviadas, o histórico de mensagens anteriores, mapa de calor com a ultima geolocalização registrada dos usuarios (aberto para novas ideias) 
- Dashboard API:
  + Backend do painel administrativo, microsserviço externo, pode ser utiizada qualquer linguagem, desde que o retorno siga os padrões JSON - RESTFULL
- Data API:
  + Camada de interação com o banco de dados, essa API será a "dona" de todas as entidades e fará toda a comunicação com o banco de dados, deve ser a primeira camada de serviço feita.
  + Deve ser utilizado MONGODB pois facilita E MUITO o desenvolvimento.
- Notification API
  + Será responsável pelo gerenciamento e entrega das notificações push, emails e SMS's
  + Para PUSH, podemos utilizar o One Signal.
  + Para SMS podemos utilizar o Plivo ou ZEnvia - Ou achar alguma solução gratuita.
  + Procurar soluções de SMS com SHORTCODE seria interessante.

## APP
  Deve ser desenvolvido um aplicativo visualmente simples, com FLUTTER, REACT NATIVE ou KOTLIN, se comunicando via API com o DATA API e o NOTIFICATION API. Deve funcionar em celulares mais antigos, IOS e Android.
  
### APP FEATURES
Algumas features do app são:
- Login e cadastro via Facebook (alta prioridade)
- Login e cadastro via SMS (alta prioridade)
- Seleção manual da cidade, uma vez após cadastro, e opção de trocar de cidade a qualquer momento depois. (alta prioridade)
- Histórico de mensagens enviadas anteriormente pela prefeitura. (alta prioridade)
- Comentários de cidadãos sobre uma determinada mensagem. (média prioridade)
- Resposta recursiva de comentários. (média prioridade)
- Envio de mensagem dos cidadãos para a prefeitura, com foto e/ou vídeo para reclamações e problemas (baixa prioridade)

