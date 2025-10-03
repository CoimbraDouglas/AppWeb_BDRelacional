README.md pronto (modelo para seu repo)

Cole esse conteúdo no README.md do repositório.

# CRUD com SQL — Banco de Dados: Escola (MariaDB / XAMPP)

## Descrição
Projeto didático para praticar comandos SQL básicos (CREATE, READ, UPDATE, DELETE) usando MariaDB via XAMPP/phpMyAdmin.
A tabela principal é `alunos`, que armazena informações básicas de estudantes.

## Pré-requisitos
- XAMPP instalado (Apache + MySQL).
- Acesso ao phpMyAdmin (http://localhost/phpmyadmin).

## Importando o banco (phpMyAdmin)
1. Abra `http://localhost/phpmyadmin`.
2. Vá em **Importar** e selecione `db/escola.sql` (ou cole o conteúdo na aba SQL).
3. Execute; o banco `escola` e a tabela `alunos` serão criados com 5 registros de exemplo.

## Comandos SQL (principais)
**Criar banco e tabela (já presente em `db/escola.sql`):**
```sql
CREATE DATABASE escola;
USE escola;
CREATE TABLE alunos (...);


Inserir (exemplos já no arquivo):

INSERT INTO alunos (nome, email, data_nascimento, curso, ativo) VALUES (...);


Listar todos:

SELECT * FROM alunos;


Listar apenas ativos:

SELECT * FROM alunos WHERE ativo = 1;


Buscar por curso:

SELECT * FROM alunos WHERE curso = 'Engenharia de Software';


Ordenar por nome:

SELECT * FROM alunos ORDER BY nome;


Atualizar curso de um aluno (ex):

UPDATE alunos SET curso = 'Marketing' WHERE id = 2;


Deletar aluno por id (ex):

DELETE FROM alunos WHERE id = 5;

Observações

No XAMPP, o usuário root normalmente não tem senha. Se você configurou senha, use-a ao importar.

Os tipos: TINYINT(1) é usado para o campo ativo (0 = inativo, 1 = ativo).

Esse projeto tem fins didáticos; em produção, o gerenciamento de senhas e usuários deve seguir boas práticas.
