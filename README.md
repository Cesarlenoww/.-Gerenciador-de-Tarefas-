Configuração e Inicialização:

Flask, SQLAlchemy e Flask-Login são importados e configurados.
A URI do banco de dados é definida como 'sqlite:///database.db' e a chave secreta para sessões é definida.
Modelos:

User: Representa um usuário com id, username e password.
Task: Representa uma tarefa com id, description e uma referência ao user_id.
Função load_user:

Carrega o usuário com base no ID armazenado na sessão.
Rotas de Autenticação:

/login: Permite aos usuários fazer login. Se o usuário e a senha forem válidos, a sessão é iniciada.
/signup: Permite novos usuários se registrarem. Eles devem fornecer um nome de usuário e senha.
/logout: Faz logout do usuário e redireciona para a página de login.
Rotas para Gerenciamento de Tarefas:

/: Exibe todas as tarefas do usuário logado.
/add: Adiciona uma nova tarefa ao banco de dados para o usuário atual.
/delete/<int:id>: Remove uma tarefa específica do banco de dados.
Execução da Aplicação:

A aplicação é executada com o modo de depuração ativado.
