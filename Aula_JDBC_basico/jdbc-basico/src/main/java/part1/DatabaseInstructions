////////////////////////////////////////////////////////
////// INSTRUÇÕES PARA INSTALAR BANCO DE DADOS /////////
////////////////////////////////////////////////////////

========================================================
======================= MYSQL ==========================
========================================================

!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! ATENÇÃO !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
OS PASSOS ABAIXO FORAM UTILIZADOS PARA INSTALAR O MYSQL NO UBUNTU 18.04.
OUTRAS VERSÕES OU SISTEMAS OPERACIONAIS DEVERÃO UTILIZAR OUTRAS REFERẼNCIAS
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! ATENÇÃO !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

==========================
1 - === INSTALAR MYSQL ===
==========================

1 - Atualizar repositório
sudo apt update

2 - Instalar MySQL
sudo apt install mysql-server

3 - Verificar se instalação foi um sucesso (deve aparecer a versão do MySQL instalado).
mysql --version

4 - (OPCIONAL) (NÂO UTILIZEI NA AULA E NÂO SERÁ NECESSÀRIO PARA AS OUTRAS ETAPAS!) Trocar valores defaults para aumentar segurança
sudo mysql_secure_installation


======================================
2 - === CONFIGURAR USUÁRIO E SENHA ===
======================================

1 - Acessar banco de dados MySQL
sudo mysql

2 - Adicionar senha "password" ao usuário "root" (Rodar no prompt do  MySQL)
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

3 - Recarregar permissões de acesso ao banco de dados (Rodar no prompt do  MySQL)
FLUSH PRIVILEGES;

4 - Sair do prompt do MySQL
quit;

Obs: A partir de agora, para acessar o mysql deverá ser utilizado o comando abaixo.
Quando pedir a senha, deverá colocar a senha: password
mysql -u root -p

===============================================
3 - === INSTALAR MYSQL WORKBENCH (OPCIONAL) ===
===============================================

1 - Atualizar repositório
sudo apt update

2 - Instalar MySQL Workbench
sudo apt install mysql-workbench

3 - Executar MySQL Workbench (também pode executar ao pesquisar por "workbench" em uma GUI do linux)
mysql-workbench


================================
4 - === CRIAR BANCO DE DADOS ===
================================

1 - Acessar banco de dados. Pode ser workbench ou linha de comando (conforme o comando abaixo)
mysql -u root -p
(Enter password:) password

2 - Criar um banco de dados (rodar no prompt do MySQL OU no MySQL workbench)
CREATE database digital_innovation_one;

3 - Usar o banco recém criado (digital_innovation_one) (rodar no prompt do MySQL OU no MySQL workbench)
USE digital_innovation_one;


============================
5 - === CRIAR UMA TABELA ===
============================

1 - Acessar banco de dados. Pode ser workbench ou linha de comando (conforme o comando abaixo)
mysql -u root -p
(Enter password:) password

2 - (CASO NÂO ESTEJA NO BANCO DE DADOS) Mudar para o banco digital_innovation_one (rodar no prompt do MySQL OU no MySQL workbench)
USE digital_innovation_one;

3 - Criar uma tabela no banco de dados (rodar no prompt do MySQL OU no MySQL workbench)
CREATE TABLE aluno (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(80) NOT NULL,
    idade INTEGER NOT NULL,
    estado CHARACTER(2) NOT NULL
);

4 - Adicionar alguns exemplos (rodar no prompt do MySQL OU no MySQL workbench)
INSERT INTO aluno(nome, idade, estado) VALUES ('Pedro', 20, 'RJ');
INSERT INTO aluno(nome, idade, estado) VALUES ('Maria', 35, 'AC');
INSERT INTO aluno(nome, idade, estado) VALUES ('Joao', 10, 'SC');
INSERT INTO aluno(nome, idade, estado) VALUES ('Ana', 51, 'GO');




!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! ATENÇÃO !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
O PASSO ABAIXO É NECESSÁRIO PARA EXECUTAR AS PRÓXIMAS TAREFAS DA PART2 e PART3

O PASSO ABAIXO FOI UTILIZADO EM UM PROJETO GRADLE
CASO ESTEJA USANDO MAVEN (ou nenhum gerenciador de pacotes) DEVERÁ SER UTILIZADO OUTRO GUIA
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! ATENÇÃO !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!


=======================================================
=== BAIXAR DRIVER PARA O JAVA SE COMUNICAR COM O BD ===
=======================================================

- No gradle deve-se adicionar no "build.gradle" (na parte de "dependencies") a linha abaixo
compile group: 'mysql', name: 'mysql-connector-java', version: '8.0.17'