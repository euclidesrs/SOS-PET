# Documentação do Projeto

## SOS-PET
### Sistema Web para Resgate, Abrigo e Adoção de Animais



Autor: Euclides Silveira

-----

# Resumo do Projeto

O SOS-PET é um sistema web desenvolvido para auxiliar instituições, ONGs e voluntários no gerenciamento de animais resgatados, oferecendo uma plataforma centralizada para cadastro, acompanhamento e adoção dos animais. Atualmente, muitas organizações utilizam planilhas ou registros manuais, tornando o controle das informações mais demorado e sujeito a erros. O sistema proposto reúne em um único ambiente o gerenciamento de animais, voluntários, abrigos e processos de adoção, proporcionando maior organização, agilidade e segurança no tratamento das informações. Como resultado, espera-se facilitar a administração das atividades relacionadas ao resgate e adoção de animais, contribuindo para um atendimento mais eficiente.

 Definição do Problema

Diversas organizações de proteção animal enfrentam dificuldades no gerenciamento das informações relacionadas aos animais resgatados, voluntários e adoções. Em muitos casos, os dados são armazenados em planilhas, documentos físicos ou aplicativos não integrados, dificultando consultas, atualizações e geração de relatórios.

Além disso, a ausência de um sistema centralizado dificulta o acompanhamento do histórico dos animais, do processo de adoção e da disponibilidade de vagas nos abrigos. Esse cenário pode ocasionar perda de informações, retrabalho e atrasos nas atividades administrativas.

O projeto SOS-PET busca solucionar esse problema por meio de um sistema web integrado, permitindo que todas essas informações sejam armazenadas em um banco de dados único e acessadas por meio de uma interface intuitiva.

 Benchmarking

Antes do desenvolvimento do SOS-PET, foi realizada uma análise de algumas plataformas voltadas para adoção e proteção animal. O objetivo foi identificar funcionalidades existentes e definir quais recursos seriam implementados no projeto.

| Funcionalidade | SOS-PET | Adopet | Petlove Adote | Adote um Gatinho |
|---|---|---|---|---|
| Cadastro de Animais | ✔ | ✔ | ✔ | ✔ |
| Cadastro de Voluntários | ✔ | ✖ | ✖ | ✖ |
| Cadastro de Abrigos | ✔ | ✔ | ✔ | ✔ |
| Controle de Adoções | ✔ | ✔ | ✔ | ✔ |
| Dashboard Administrativo | ✔ | ✖ | ✖ | ✖ |
| Relatórios | ✔ | ✖ | ✖ | ✖ |
| Pesquisa de Animais | ✔ | ✔ | ✔ | ✔ |
| Interface Responsiva | ✔ | ✔ | ✔ | ✔ |

# Análise

A comparação demonstra que os sistemas pesquisados possuem funcionalidades voltadas principalmente para divulgação e adoção de animais. O SOS-PET diferencia-se por reunir, em uma única plataforma, recursos de gerenciamento administrativo, cadastro de voluntários, controle de abrigos, relatórios e painel de indicadores, oferecendo maior suporte à gestão de instituições responsáveis pelo resgate e adoção de animais.

## Objetivos

### Objetivo Geral

Desenvolver um sistema web para gerenciamento de animais resgatados, voluntários, abrigos e processos de adoção, proporcionando maior organização, controle e eficiência às instituições responsáveis pelo cuidado dos animais.

### Objetivos Específicos

* Cadastrar animais resgatados.
* Gerenciar informações dos voluntários.
* Controlar os abrigos cadastrados.
* Registrar processos de adoção.
* Disponibilizar consultas e filtros de pesquisa.
* Gerar relatórios para apoio à gestão.

## Stack Tecnológico

O desenvolvimento do SOS-PET utilizará tecnologias amplamente empregadas no desenvolvimento de aplicações web, priorizando desempenho, organização do código e facilidade de manutenção.

O Vue.js será utilizado no desenvolvimento da interface do sistema (frontend), proporcionando uma experiência responsiva e intuitiva ao usuário.

O Node.js, juntamente com o framework Express.js, será responsável pelo desenvolvimento da API REST, permitindo a comunicação entre a interface do sistema e o banco de dados.

O banco de dados utilizado será o MySQL, escolhido por sua confiabilidade, facilidade de administração e ampla utilização em aplicações web.

Para facilitar o mapeamento entre as tabelas do banco de dados e os objetos da aplicação será utilizado o Sequelize, que oferece recursos para criação de modelos, relacionamentos e migrações.

Durante os testes da API será utilizado o Insomnia, permitindo validar todas as rotas desenvolvidas. Os testes automatizados serão implementados utilizando Jest, garantindo o funcionamento das principais funcionalidades do sistema.

O versionamento do projeto será realizado utilizando Git e GitHub, possibilitando o controle das alterações realizadas durante o desenvolvimento.

O ambiente de desenvolvimento utilizado será o Visual Studio Code, devido à sua integração com as tecnologias adotadas e ao amplo suporte por meio de extensões.

## Descrição da Solução

O SOS-PET será desenvolvido como uma aplicação web composta por um frontend, uma API REST e um banco de dados relacional.

Após realizar o login, o administrador terá acesso a um painel inicial contendo informações gerais do sistema, como quantidade de animais cadastrados, adoções realizadas, voluntários ativos e abrigos registrados.

O sistema permitirá cadastrar, consultar, editar e excluir animais resgatados, armazenando informações como nome, espécie, raça, idade, porte, situação, descrição e fotografia.

Também será possível cadastrar voluntários responsáveis pelo atendimento aos animais, além de registrar os abrigos parceiros e sua capacidade de atendimento.

Quando um animal for adotado, o sistema registrará automaticamente a adoção, alterando seu status para "Adotado", impedindo novas adoções para o mesmo animal.

Além das operações de cadastro, o sistema contará com recursos de pesquisa, filtros e relatórios simples, facilitando o gerenciamento das informações e apoiando a tomada de decisão pelos responsáveis pela instituição.

## Arquitetura

O projeto seguirá uma arquitetura em camadas, separando a aplicação em Frontend, Backend e Banco de Dados.

O frontend será desenvolvido utilizando Vue.js, responsável pela interface apresentada ao usuário.

O backend será desenvolvido em Node.js com Express.js, implementando uma API REST responsável pelas regras de negócio e comunicação com o banco de dados.

O banco de dados MySQL armazenará todas as informações do sistema de forma estruturada e segura.

Durante o desenvolvimento do projeto foram elaborados os seguintes artefatos para auxiliar na análise, planejamento e implementação da solução: Benchmarking (tabela comparativa), Persona, Casos de Uso, Diagrama Entidade-Relacionamento (DER) e Wireframes. Esses artefatos permitiram definir os requisitos do sistema, modelar o banco de dados, compreender o perfil dos usuários e projetar a interface da aplicação.

> **Repositório do projeto:** _[inserir link do GitHub aqui]_

## Validação

A validação do sistema será realizada por meio de testes funcionais das principais funcionalidades, verificando se os requisitos definidos para o projeto foram atendidos. Serão realizados testes de cadastro, consulta, atualização e exclusão de registros, além da validação do fluxo completo de adoção de um animal. Também será verificada a integração entre o frontend, a API REST e o banco de dados, garantindo que as informações sejam armazenadas e recuperadas corretamente.

### Estratégia

O desenvolvimento será realizado de forma incremental, implementando cada módulo separadamente e realizando testes após sua conclusão. Inicialmente serão desenvolvidas as funcionalidades de autenticação, cadastro de animais, voluntários e abrigos. Em seguida será implementado o módulo de adoção e, por fim, os recursos de pesquisa, filtros e relatórios. Essa estratégia permitirá identificar possíveis problemas durante o desenvolvimento e facilitará a evolução do sistema.

## Consolidação dos Dados Coletados

Ao término do desenvolvimento, serão apresentados os resultados obtidos por meio dos testes realizados. Será verificado se todos os requisitos funcionais foram implementados corretamente, bem como o desempenho das operações principais do sistema. Os resultados obtidos servirão para comprovar o funcionamento da solução proposta e identificar possíveis melhorias futuras.

## Conclusões

O desenvolvimento do SOS-PET busca oferecer uma solução tecnológica para auxiliar instituições e voluntários no gerenciamento de animais resgatados e processos de adoção. A informatização desses processos permitirá maior organização das informações, redução de erros, facilidade de consulta e melhoria na administração das atividades relacionadas ao cuidado dos animais.

Além de atender aos objetivos propostos, o projeto proporcionará experiência prática no desenvolvimento de aplicações web utilizando tecnologias atuais, integrando frontend, backend e banco de dados em uma única solução.

## Limitações do Projeto e Perspectivas Futuras

Nesta versão do sistema serão implementadas apenas as funcionalidades essenciais para o gerenciamento de animais, voluntários, abrigos e adoções.

Como trabalhos futuros, poderão ser adicionadas funcionalidades como:

* Aplicativo para dispositivos móveis;
* Cadastro de adotantes com histórico completo;
* Notificações por e-mail;
* Integração com serviços de mapas para localização de abrigos;
* Painel administrativo mais completo com gráficos e indicadores;
* Controle de campanhas de arrecadação e eventos.

## Referências Bibliográficas

ADOPET. **Plataforma de adoção responsável de animais**. Disponível em: https://adopet.com.br/. Acesso em: 26 jun. 2026.

ADOTE UM GATINHO. **Organização de proteção animal**. Disponível em: https://www.adoteumgatinho.org.br/. Acesso em: 26 jun. 2026.

EXPRESS.JS. **Documentação Oficial**. Disponível em: https://expressjs.com/. Acesso em: 26 jun. 2026.

GITHUB. **Documentação Oficial**. Disponível em: https://github.com/. Acesso em: 26 jun. 2026.

JEST. **Documentação Oficial**. Disponível em: https://jestjs.io/. Acesso em: 26 jun. 2026.

MYSQL. **Documentação Oficial**. Disponível em: https://dev.mysql.com/doc/. Acesso em: 26 jun. 2026.

NODE.JS. **Documentação Oficial**. Disponível em: https://nodejs.org/. Acesso em: 26 jun. 2026.

PETLOVE ADOTE. **Plataforma de adoção de animais**. Disponível em: https://adote.petlove.com.br/. Acesso em: 26 jun. 2026.

SEQUELIZE. **Documentação Oficial**. Disponível em: https://sequelize.org/. Acesso em: 26 jun. 2026.

VUE.JS. **Documentação Oficial**. Disponível em: https://vuejs.org/. Acesso em: 26 jun. 2026.

