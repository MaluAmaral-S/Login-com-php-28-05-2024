# Sistema de Autenticação com PHP e AJAX

Este projeto é uma implementação de um sistema de login funcional que utiliza comunicação assíncrona para validar credenciais. O foco principal é demonstrar o fluxo de autenticação, desde a interface do usuário até a persistência de dados e proteção de rotas via sessões.

## Funcionalidades Principais

* **Login Assíncrono:** Utiliza jQuery e AJAX para enviar credenciais ao servidor sem a necessidade de recarregar a página, melhorando a experiência do usuário (UX).
* **Validação de Erros:** Exibe mensagens dinâmicas para usuários não encontrados ou senhas incorretas diretamente na tela de login.
* **Gestão de Sessões:** Protege páginas internas, garantindo que apenas usuários autenticados acessem a área logada.
* **Segurança com PDO:** A conexão com o banco de dados e as consultas utilizam *Prepared Statements*, prevenindo ataques de SQL Injection.

## Tecnologias Utilizadas

* **Backend:** PHP com extensão PDO para interação com banco de dados MySQL.
* **Frontend:** HTML5, CSS3 e Bootstrap 5 para uma interface responsiva.
* **Client-side Scripting:** JavaScript com a biblioteca jQuery para requisições AJAX.
* **Servidor de Banco de Dados:** MySQL.

## Estrutura do Projeto

* `db.php`: Configuração da conexão PDO com o banco de dados.
* `login.php`: Lógica de validação de credenciais e inicialização da sessão.
* `validacao.js`: Script responsável por capturar o evento de clique, realizar a chamada AJAX e tratar as respostas do servidor.
* `pagina_login.html`: Interface visual do sistema de login.
* `pagina_secundaria.php`: Página restrita que exibe as informações do usuário logado.
* `pagina_logout.php`: Encerramento da sessão e redirecionamento seguro.

## Como Executar

1. Certifique-se de ter um ambiente de servidor local (como XAMPP, WAMP ou Docker).
2. Crie um banco de dados chamado `clientes` no MySQL.
3. Crie uma tabela chamada `clientes` com os campos `nome` e `senha`.
4. Configure as credenciais de acesso no arquivo `db.php`.
5. Acesse `pagina_login.html` através do seu navegador via `localhost`.

---

**Nota Técnica:** Este projeto foi desenvolvido para fins didáticos. Em um ambiente de produção real, é recomendada a implementação de hash de senhas (BCRYPT) e camadas adicionais de validação de dados.
