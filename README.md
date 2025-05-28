Sistema de Gestão de Ordem de Serviços
Descrição do Projeto
Este projeto, desenvolvido por Renan Weiber para a disciplina Padrões de Desenvolvimento de Software em Java do curso de Análise e Desenvolvimento de Sistemas (ADS) na Faculdade Estácio de Curitiba, é um sistema de gerenciamento de ordens de serviço. Ele facilita o cadastro, controle e acompanhamento de serviços prestados, clientes, técnicos e status das ordens. 
Desenvolvido em Java com interface gráfica desktop utilizando Swing, o projeto segue o padrão arquitetural MVC (Model-View-Controller) para garantir organização, escalabilidade e facilidade de manutenção do código.
Funcionalidades Principais

Cadastro e gerenciamento de clientes e técnicos.
Registro e acompanhamento de ordens de serviço.
Controle de status das ordens (aberta, em andamento, finalizada).
Geração de relatórios básicos para monitoramento dos serviços realizados.
Interface gráfica desktop intuitiva, desenvolvida com Java Swing.

Tecnologias Utilizadas

Linguagem: Java
Interface Gráfica: Java Swing
Arquitetura: MVC (Model-View-Controller)
Banco de Dados: MySQL
Testes Automatizados: JUnit
IDE Utilizada: Visual Studio Code (VSCode)

Instruções para Execução
Pré-requisitos
Antes de começar, certifique-se de ter os seguintes itens instalados:

Java JDK 8 ou superior: Necessário para compilar e executar o aplicativo Java.
Git: Para clonar o repositório do projeto.
XAMPP: Para rodar o servidor MySQL localmente.
MySQL: Banco de dados configurado e funcionando via XAMPP.
Navegador Web: Para acessar o phpMyAdmin.

Passo a Passo para Clonar e Rodar o Projeto

Clonar o projeto do GitHubAbra o terminal e execute o comando abaixo para clonar o repositório:
git clone https://github.com/Rweiber/GestorOS.git

Isso criará uma pasta chamada GestorOS com os arquivos do projeto.

Entrar na pasta do projetoNavegue até a pasta clonada:
cd GestorOS


Configurar o banco de dadosa. Acesse o phpMyAdmin:   No navegador, abra:
http://localhost/phpmyadmin

b. Crie o banco de dados:  

Clique em "Novo".
Nomeie o banco como dbinfox.
Clique em "Criar".

c. Execute o script SQL:   Com o banco dbinfox selecionado:  

Clique na aba "SQL".
Cole o seguinte script:create table tbusuarios(
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


Clique em "Executar" para criar as tabelas e inserir o usuário padrão.


Rodar o aplicativo Javaa. Baixe o JAR do sistema:  

Acesse o link: https://github.com/Rweiber/GestorOS/releases/tag/v1.0.
Baixe o arquivo prjinfoX.zip.
Extraia o conteúdo para obter o arquivo prjinfoX.jar.

b. Execute o sistema:   No terminal, ou clicando duas vezes no arquivo .jar, execute:
java -jar prjinfoX.jar

   Nota: Certifique-se de que o XAMPP (MySQL) esteja rodando antes de executar o aplicativo.

Login no sistemaUse as credenciais abaixo para acessar o sistema:

Usuário: admin
Senha: adminSe o ícone do banco de dados no login estiver verde, a conexão com o banco foi estabelecida com sucesso.



Execução Alternativa (via IDE)

Abra o projeto no Visual Studio Code.
Configure as dependências e a conexão com o banco no arquivo de configuração do projeto.
Compile e execute a aplicação Java.
A interface gráfica Swing será exibida para uso.

Estrutura do Projeto

Model: Contém as classes que representam as entidades do sistema, como Cliente, Técnico e Ordem de Serviço.
View: Inclui as telas e componentes gráficos desenvolvidos com Java Swing.
Controller: Classes responsáveis pela lógica de negócios e pela interação entre Model e View.
Testes: Testes unitários implementados com JUnit para garantir a qualidade e robustez do código.

Autor
Renan WeiberAluno do curso de Análise e Desenvolvimento de Sistemas (ADS)Faculdade Estácio de CuritibaDisciplina: Padrões de Desenvolvimento de Software em Java
Contato
Para dúvidas, sugestões ou contribuições, entre em contato pelo e-mail: hideoutrws2@gmail.com.
Licença
Este projeto é distribuído sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
