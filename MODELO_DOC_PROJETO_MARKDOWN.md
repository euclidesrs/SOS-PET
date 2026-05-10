# Documentação do Projeto 

## Nome do Autor

Euclides Roberto da Silveira

---

## Resumo do Projeto

Este projeto tem como objetivo desenvolver uma API REST para gerenciamento de um petshop, permitindo o cadastro de animais, serviços e o agendamento de atendimentos.

O problema abordado está na dificuldade de organizar e controlar serviços de forma eficiente, especialmente quando realizado manualmente.

A solução proposta consiste em um sistema backend que centraliza essas informações, facilitando o gerenciamento e reduzindo erros operacionais.

Com isso, espera-se melhorar a organização do petshop e otimizar o controle dos serviços prestados.

---

## Definição do Problema

Atualmente, muitos petshops utilizam métodos manuais ou sistemas pouco eficientes para gerenciar seus serviços, o que pode gerar perda de dados, desorganização e dificuldades operacionais no dia a dia.

Grande parte dos estabelecimentos de menor porte ainda opera sem sistemas informatizados adequados, o que impacta diretamente na experiência do cliente, que espera um atendimento personalizado e eficiente.

Além disso, não há uma integração clara entre animais, serviços realizados e agendamentos, dificultando o controle das operações e a rastreabilidade dos atendimentos prestados.

Dessa forma, surge a necessidade de uma solução tecnológica que centralize essas informações e permita um gerenciamento mais eficiente.

---

## Objetivos

### Objetivo Geral

Desenvolver uma API REST para gerenciamento de um petshop.

### Objetivos Específicos

- Cadastrar animais
- Cadastrar serviços
- Permitir agendamento de serviços
- Implementar tratamento de erros
- Criar testes automatizados com Jest
- Garantir organização e consistência dos dados

---


## Pilha Tecnológica

- Node.js
- Express.js
- PostgreSQL
- Jest
- Insomnia
- Git
- GitHub

## Motivo das Escolhas Tecnológicas

O desenvolvimento da aplicação foi realizado utilizando Node.js como ambiente de execução JavaScript no lado servidor. A escolha dessa tecnologia ocorreu devido ao seu modelo assíncrono e orientado a eventos, proporcionando bom desempenho e escalabilidade para aplicações web modernas (NODE.JS FOUNDATION, 2026).

O framework Express.js foi utilizado para estruturar a API REST devido à sua simplicidade, flexibilidade e ampla adoção no desenvolvimento backend com JavaScript, permitindo implementação eficiente de rotas, middlewares e tratamento centralizado de erros (EXPRESS, 2026).

Para persistência dos dados foi adotado o PostgreSQL, sistema gerenciador de banco de dados relacional reconhecido pela robustez, confiabilidade transacional e conformidade com padrões SQL (POSTGRESQL, 2026).

A validação automatizada da aplicação será realizada utilizando Jest, framework amplamente empregado no ecossistema JavaScript por sua praticidade e suporte nativo a testes assíncronos (JEST, 2026).

O versionamento será realizado com Git e o armazenamento remoto no GitHub, possibilitando rastreabilidade, controle de versões e organização do desenvolvimento (CHACON; STRAUB, 2014).

As requisições e testes manuais da API serão executados por meio do Insomnia, ferramenta voltada à validação e depuração de APIs REST (INSOMNIA, 2026).


---

## Descrição da Solução

A solução consiste em uma API REST desenvolvida com Node.js e Express, com persistência de dados em banco PostgreSQL.

O sistema foi projetado seguindo os princípios RESTful, utilizando os verbos HTTP de forma semântica:

- GET para consulta
- POST para criação
- PUT para atualização
- DELETE para remoção

As respostas são retornadas no formato JSON.

O sistema é composto por três entidades principais: Animais, Serviços e Agendamentos.

A entidade Animal armazena dados do pet, como nome, espécie e raça, além das informações do tutor, incluindo nome e contato.

A entidade Serviço registra os tipos de atendimento oferecidos pelo petshop, como banho e tosa, consulta veterinária e hospedagem.

A entidade Agendamento relaciona um animal a um serviço, registrando data, horário e status do atendimento, podendo estar como pendente, concluído ou cancelado.

A aplicação conta com tratamento centralizado de erros, retornando códigos HTTP adequados em cada situação:

- 400 para requisições inválidas
- 404 para recursos não encontrados
- 500 para erros internos do servidor

Cada endpoint realiza validação dos dados de entrada antes de qualquer operação no banco de dados.

A segurança básica é garantida pela validação em nível de aplicação e pelas constraints do banco PostgreSQL.

Como perspectiva futura, está prevista a implementação de autenticação via JWT (JSON Web Token) para controle de acesso.

---

## Arquitetura

A aplicação segue o padrão de arquitetura REST, organizada em camadas:

### Rotas
Responsáveis por receber as requisições HTTP.

### Controllers
Tratam a lógica da aplicação.

### Models
Representam as entidades e regras de persistência.

### Banco de Dados
Responsável pelo armazenamento das informações.

A comunicação ocorre via protocolo HTTP utilizando operações CRUD.

---

## Validação

Serão realizados testes automatizados utilizando Jest para validar o funcionamento da API.

Os testes incluem cenários de sucesso e erro, garantindo maior confiabilidade da aplicação.

Até o momento, não foram realizadas sessões formais de testes de aceitação com usuários finais.

Entretanto, futuramente serão conduzidas avaliações práticas nas quais os usuários serão orientados a executar tarefas específicas, como:

- Cadastrar um animal
- Agendar um serviço
- Consultar histórico de atendimentos

O objetivo será avaliar clareza das respostas, consistência das operações e facilidade de integração com interfaces consumidoras da API.

---

## Consolidação dos Dados Coletados

A API permite:

- Listar animais cadastrados
- Consultar serviços disponíveis
- Visualizar agendamentos realizados
- Monitorar status dos atendimentos

Essas funcionalidades contribuem para maior organização e controle das operações internas do petshop.

---

## Conclusão

Este projeto teve como objetivo resolver um problema real enfrentado por petshops de pequeno e médio porte: a ausência de um sistema centralizado e eficiente para gerenciar animais, serviços e agendamentos.

A API REST desenvolvida com Node.js, Express e PostgreSQL atende a esse objetivo ao oferecer endpoints funcionais, tratamento adequado de erros e cobertura por testes automatizados.

O projeto demonstra a aplicação prática de conceitos fundamentais de desenvolvimento de software, como arquitetura REST, separação de responsabilidades em camadas, qualidade de código por meio de testes e versionamento utilizando Git.

A solução desenvolvida é funcional, documentada e representa uma base escalável para futuras evoluções, como autenticação de usuários e desenvolvimento de interface gráfica.

---

## Limitações do Projeto e Perspectivas Futuras

Atualmente, o sistema apresenta algumas limitações:

- Não possui interface gráfica
- Não possui autenticação de usuários
- Não possui notificações automáticas
- Não possui painel administrativo visual

Como melhorias futuras, pretende-se implementar:

- Frontend web
- Autenticação JWT
- Controle de permissões
- Dashboard administrativo
- Histórico detalhado de atendimentos

---

## Referências Bibliográficas

ABINPET. Mercado Pet Brasil 2023. São Paulo: Associação Brasileira da Indústria de Produtos para Animais de Estimação, 2023. Disponível em: http://abinpet.org.br. Acesso em: mai. 2026.
CHACON, Scott; STRAUB, Ben. Pro Git. 2. ed. Nova York: Apress, 2014. Disponível em: https://git-scm.com/book/en/v2. Acesso em: mai. 2026.
EXPRESS. Express.js Documentation. Disponível em: https://expressjs.com. Acesso em: mai. 2026.
ISO/IEC 25010:2011. Systems and software engineering - Systems and software Quality Requirements and Evaluation (SQuaRE). Geneva: ISO, 2011.
JEST. Jest Documentation. Disponível em: https://jestjs.io. Acesso em: mai. 2026.
NODE.JS FOUNDATION. Node.js Documentation. Disponível em: https://nodejs.org/en/docs. Acesso em: mai. 2026.
POSTGRESQL. PostgreSQL Documentation. Disponível em: https://www.postgresql.org/docs. Acesso em: mai. 2026.
SOMMERVILLE, Ian. Engenharia de Software. 9. ed. São Paulo: Pearson, 2011.
INSOMNIA. Insomnia REST Client Documentation. Disponível em: https://docs.insomnia.rest. Acesso em: mai. 2026.
Materiais acadêmicos da disciplina Projeto de Desenvolvimento II.
