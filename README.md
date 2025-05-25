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

### Pré-requisitos

- Java JDK 8 ou superior.
- Banco de dados MySQL rodando com o schema do projeto importado.

### Configuração

1. Ajustar as configurações de conexão com o banco no arquivo de configuração do projeto.
2. Importar o script SQL para criar as tabelas necessárias.

### Execução

1. Abrir o projeto no Visual Studio Code.
2. Compilar e executar a aplicação Java.
3. A interface Swing será exibida como aplicação desktop para uso.

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

You can copy the content within the `<xaiArtifact>` tags and paste it directly into your project's `README.md` file.
