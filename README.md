# Sistema de controle de acesso

## Detalhes técnicos:
<em>Sistema sendo desenvolvido em PHP 7.4+, usando a arquitetura MVC (POO), CoffeeCode DataLayer como ORM, banco de dados MySQL</em>

Necessário para o funcionamento do sistema: PHP 7.4+, MySQL, Composer, GIT (para clonar o repositório, caso queira).

- Usuário Admin: "admin", senha: "123"

## Procedimentos para instalação local:

- Baixe o projeto em uma pasta
- Acesse a pasta via linha de comando
- Execute o comando: <code>composer update</code> para baixar as dependências do projeto
- No MySQL crie um banco com o nome <code>portaria_db</code>
- Rode o script <code>docs/tabelas.sql</code> no banco para criar as tabelas do sistema
  - Será criado o usuário "admin" no banco, senha "123", com acesso ao ambiente administrativo.
- Ajuste as configurações de acesso ao banco de dados no arquivo <code>src/config.php</code>
- Crie o arquivo <code>src/configemail.php</code> para ajustar as configurações de envio de e-mail, caso queira utilizar essa opção
  - Neste arquivo deverão ser informadas as segunites configurações:
  - <code>$email_remetente = 'remetente@email.com';</code> <i> Remetente do e-mail </i>
  - <code>$email_servidor = 'smtp.servidor.com';</code> <i> Host, endereço do servidor de disparo de e-mails (SMTP) </i>
  - <code>$email_usuario = 'login@email.com';</code> <i> Login da conta de e-mail </i>
  - <code>$email_senha = '123456';</code> <i> Senha da conta de e-mail </i>