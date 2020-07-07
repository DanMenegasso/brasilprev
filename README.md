# Proposta
Você foi convidado a realizar um desafio para a vaga de desenvolvedor(a) back-end Python. Queremos avaliar sua qualidade de código, capacidade de análise, resolução de problemas e principalmente sua criatividade.

Construa uma API REST para simular uma loja virtual. Esta loja deve ter um cadastro de seus clientes, produtos e pedidos. Fique à vontade para escolher como fará a arquitetura do sistema, bem como frameworks que utilizará.


# Tecnologias utilizadas
Foi utilizado o framework Flask para o desenvolvimento do sistema, com um banco local sqlite versão 3, mas pode ser substituido qualquer banco que seja SQL ou similar (SQL, PostgreSQL, Oracle, MariaDB, etc). Para o login é utilizado JWT.

Para os testes foi utilizada a biblioteca pytest, que faz testes unitários e de integração.

O sistema possui recuperação de senha. Caso queira ativá-lo, inserir os dados corretos no \"environment\".O sistema foi desenvolvido com base no SES da AWS com emails reais dentro e fora da sandbox.

# O sistema abrange
- Perfilamento simples
- Login
- Recuperação de senha
- CRUD de usuário
- CRUD de produtos
- CRUD de fornecedores
- CRU de pedidos

# Fluxo de Informação
## Admin

O admin é responsável por:
- cadastrar usuários
- visualizar usuários
- editar usuários
- excluir usuários
- cadastrar produtos
- visualizar produtos
- editar produtos
- excluir produtos
- cadastrar fornecedores
- visualizar fornecedores
- editar fornecedores
- excluir fornecedores
- cadastrar pedidos
- visualizar pedidos
- editar pedidos
- excluir pedidos

## Usuário
O usuário é responsável por:
- visualizar produtos
- visualizar os próprios pedidos
- cadastrar pedidos


# Inicialização do sistema
Para inicializar o sistema, é necessário:
- Python 3.7 ou superior
- Banco SQL ou similar (caso queira usar sqlite3, apenas não altere o environment)

## Instalação
Necessário a criação de uma virtual env (para não sobrecarregar o SO) e a pasta comum de instalação padrão do Python.

Para instalar a Virtual Env:
> pip install virtualenv
> virtualenv nome-da-virtualenv

Para ativar a Virtual Env:
> activate (dentro da pasta venv/Scripts)

Para instalar as dependências, use:
> pip install -r requirements.txt

Lembre-se de atualizar o environment com as credenciais de sua preferência


## Execução
Para executar o sistema, use:
> flask run

ou:
> python application.py

Após rodar o sistema, faça uma requisição para qualquer URL, isso preenche a base de dados.
Na primeira requisição, as tabelas serão criadas automaticamente junto com as seeds de banco para inicializar o projeto.


# Testes
Foram feitos  testes unitários e de integração para validar o sistema.

Para rodar os testes, use:
> pytest tests\\models tests\\resources tests\\helpers --disable-pytest-warnings -v
