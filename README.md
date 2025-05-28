# Sistema de Gestão de Ordem de Serviços

## Descrição do Projeto

Este projeto foi desenvolvido por Renan Weiber para a disciplina Padrões de Desenvolvimento de Software em Java do curso de Análise e Desenvolvimento de Sistemas (ADS) na Faculdade Estácio de Curitiba.

O sistema tem como objetivo gerenciar ordens de serviços, facilitando o cadastro, controle e acompanhamento dos serviços prestados, clientes, técnicos e os status das ordens. Desenvolvido em Java com interface gráfica desktop utilizando Swing, estruturado segundo o padrão arquitetural MVC para garantir organização e manutenção facilitada do código.

## Funcionalidades Principais

- Cadastro e gerenciamento de clientes e técnicos.
- Registro e acompanhamento das ordens de serviço.
- Controle de status das ordens (aberta, em andamento, finalizada).
- Relatórios básicos para monitoramento dos serviços realizados.
- Interface desktop gráfica desenvolvida com Java Swing para facilitar a interação do usuário.

## Tecnologias Utilizadas

- **Linguagem**: Java
- **Interface Gráfica**: Java Swing
- **Arquitetura**: MVC (Model-View-Controller)
- **Banco de dados**: MySQL
- **Testes automatizados**: JUnit
- **IDE utilizada**: Visual Studio Code (VSCode)

## Instruções para Execução

Passo a Passo para Clonar e Rodar o Projeto infox

✅ Pré-requisitos:

Java 8 ✅

Git ✅

XAMPP rodando (MySQL funcionando)✅

🚀 1. Clonar o projeto do GitHubAbra o terminal e rode:
```bash
git clone https://github.com/Rweiber/GestorOS
```
Isso vai criar uma pasta chamada infox com o projeto dentro.

📂 2. Entrar na pasta do projeto
```bash
cd GestorOS
```
🛠️ 3. Instalar o banco de dadosA. Acesse o phpMyAdmin:Abra no navegador:

http://localhost/phpmyadmin

A. Crie o banco de dados:  

Clique em "Novo".
Nomeie como dbinfox.
Clique em "Criar".

B. Execute o SQL:Com o banco dbinfox selecionado:

Clique na aba SQL.
Cole o seguinte conteúdo:
```sql
create table tbusuarios(
    iduser int primary key,
    usuario varchar(15) not null,
    fone varchar(15),
    login varchar(15) not null unique,
    senha varchar(250) not null,
    perfil varchar(20) not null
);

insert into tbusuarios(iduser, usuario, login, senha, perfil)
values(1, 'Administrador', 'admin', md5('admin'), 'admin');

create table tbclientes(
    idcli int primary key auto_increment,
    nomecli varchar(50) not null,
    endcli varchar(100),
    fonecli varchar(15) not null,
    emailcli varchar(50) unique
);

create table tbos(
    os int primary key auto_increment,
    data_os timestamp default current_timestamp,
    tipo varchar(15) not null,
    situacao varchar(20) not null,
    equipamento varchar(150) not null,
    defeito varchar(150),
    servico varchar(150),
    tecnico varchar(30),
    valor decimal(10,2),
    idcli int not null,
    foreign key(idcli) references tbclientes(idcli)
);
```

Clique em "Executar".

📦 4. Rodar o aplicativo Java Baixe o JAR do sistema:  

Vá até este link no navegador: https://github.com/Rweiber/GestorOS/releases/tag/v1.0.

Baixe o arquivo prjinfoX.zip.

Extraia o conteúdo (vai conter prjinfoX.jar).

A. Execute o sistema:No terminal (ou clique duas vezes no .jar):
```bash
java -jar prjinfoX.jar
```
Obs: Certifique-se de estar com o XAMPP (MySQL) rodando.

✅ 5. Login no sistema
Acesse com:

Usuário: admin
Senha: admin

Se o ícone do banco no login estiver verde, está tudo certo!

## Estrutura do Projeto

- **Model**: Classes que representam entidades como Cliente, Técnico e Ordem de Serviço.
- **View**: Telas e componentes desenvolvidos em Java Swing.
- **Controller**: Classes que gerenciam a lógica e a interação entre Model e View.
- **Testes**: Testes unitários com JUnit para garantir a qualidade do código.

## Autor

Renan Weiber  
Aluno do curso de Análise e Desenvolvimento de Sistemas (ADS)  
Faculdade Estácio de Curitiba  
Disciplina: Padrões de Desenvolvimento de Software em Java

## Contato

Para dúvidas, sugestões ou contribuições, entre em contato pelo e-mail: hideoutrws2@gmail.com
