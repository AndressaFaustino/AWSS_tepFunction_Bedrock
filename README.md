# AWSS_tepFunction_Bedrock
Base de conhecimento adiquirido durante a entrega do projeto final AWS Step Functions e Bedrock

APP Pedidos

Ao realizar o pedido, o usuário tem seu usuário de pedidos e cupons em uma primeira api, após o pedido realizado o api envia notificação através do gerenciador de push notifications para somente ser encaminhado para o api de estado de pedido, gerando um fluxo para a funcionalidade em conjunto, cada passo depende de um micro serviço, apesar de funcionar isoladamente (subscriber) a comunicação de fluxo ocorre através da ferramenta agente de comunicação através dos serviços de mensageria (publisher).

Trazendo isso para a aws de maneira mais prática podemos utilizar o AWS STEP FUNCTIONS você cria o fluxo orquestrado de forma prática com blocos de clica e arrasta executando funções e serviços da aws, simplificando e agilizando o fluxo, processando dos dados sob demanda e visualizando a arquitetura por elementos padronizados conforme objetivo esperado a Saga Pattern

Para criarmos o app pela AWS, devemos seguir pela página inicial do console, serviços, integração de aplicativos e step funcions:
Começando através do Templante o projeto sempre no step funcions terá o nome de maquina de estado, um workflow, começando pelo fluxo de trabalho Hello World é utilizado oWorkflow studio para codificar os fluxos de trabalho (máquina de estado), executando ações e fluxos através do "clica e arrasta", para as definições da máquina de estado é utilizado o Amazon State Language em JSON no estilo VS Code, para customizar a aplicação podemos editar a entrada e saída, e também as variáveis através da ferramenta inspetor, e através do botão iniciar a execução pode ser realizado o teste da aplicação.
Na prática a aplicação dessa API utilizando um modelo de Encadeamento de Prompts de IA pelo  Amazon Bedrock lembrando de autorizar as permissões para executar a API através da edição de estado de máquina, configuração visualizar IAM, em cada caixinha de configuração, nesse modelo deve ser utilizado o haiku, configurando os prompts como ele solicita.

Após todas as configurações, e execução de teste com sucesso, basta seguir com a utilização e execução da API criada
