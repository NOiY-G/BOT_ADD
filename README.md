Descrição do Script

O script automatiza a adição de usuários a um canal do Telegram usando a API de administrador. Ele realiza os seguintes passos:

Importação de Bibliotecas:
 * Usa telethon para interagir com a API do Telegram.
 * Usa openpyxl para manipular o arquivo Excel.
 * Usa time para introduzir atrasos entre as adições de usuários.

Configuração Inicial:
 * Define as credenciais da API (api_id e api_hash).
 * Especifica o nome do canal (channel_username).
 * Define o nome do arquivo Excel que contém os IDs dos usuários a serem adicionados.

Função Principal (adicionar_membros_do_excel):
 * Cria uma sessão do cliente do Telegram.
 * Abre o arquivo Excel e lê os IDs dos usuários.
 * Itera sobre cada linha (a partir da segunda) no arquivo Excel.
  * Extrai o ID do usuário.
  * Obtém informações sobre o canal do Telegram.
  * Envia uma solicitação para adicionar o usuário ao canal.
  * Aguarda um intervalo de tempo (delay) entre cada adição.
  * Limita a adição a um número específico de usuários (limite).
  * Introduz uma espera prolongada após atingir o limite, antes de continuar.

Execução:
A função é chamada com um delay de 10 segundos entre cada adição e um limite de 50 usuários por sessão.

Detalhes Técnicos
 * Delay: Controla o tempo de espera entre a adição de cada usuário para evitar sobrecarga e respeitar os limites do Telegram.
 * Limite: Após atingir o limite de adições, o script aguarda uma hora antes de continuar, respeitando as restrições do Telegram.
 * Tratamento de Exceções: Captura e exibe erros que ocorrem durante o processo de adição.
 * Esse script é útil para gerenciar grandes listas de usuários e adicioná-los de maneira eficiente ao seu canal do Telegram, respeitando os limites e diretrizes da plataforma.
