# Gerenciador de Pessoas - Desafio Simbiose Ventures
Uma aplicação web completa para gerenciar um cadastro de pessoas, desenvolvida com React e Spring Boot.

## Descrição
Este projeto foi desenvolvido como resposta ao desafio técnico da Simbiose Ventures. Ele oferece uma solução completa para gerenciar um cadastro de pessoas, desde a criação até a exclusão de registros. A aplicação utiliza tecnologias modernas e robustas para garantir um alto desempenho e escalabilidade.

**Funcionalidades Principais:**
* Cadastro, atualização e exclusão de pessoas.
* Consulta detalhada de informações de cada pessoa.
* Listagem completa de todas as pessoas cadastradas.

**Tecnologias:**

* **Frontend:** React
    * Biblioteca JavaScript para construção de interfaces de usuário.
* **Backend:** Spring Boot
    * Framework Java para desenvolvimento de aplicações web.
* **Banco de dados:** PostgreSQL
    * Sistema gerenciador de banco de dados relacional, robusto e escalável.
* **Cloud:** AWS
    * Plataforma de computação em nuvem para hospedar a aplicação.
* **Ferramentas:**
    * Maven: Gerenciador de build para projetos Java.
    * npm: Gerenciador de pacotes para projetos JavaScript.
    * Docker: Plataforma de containerização para facilitar o desenvolvimento e deploy da aplicação.

## Endpoints da API
A API RESTful da aplicação expõe os seguintes endpoints:

* **GET /pessoas:** Retorna uma lista de todas as pessoas cadastradas.
* **GET /pessoas/{id}:** Retorna os detalhes de uma pessoa específica, identificada pelo seu ID.
* **POST /pessoas:** Cria uma nova pessoa. **Requer:** nome, email, data de nascimento.
* **PUT /pessoas/{id}:** Atualiza os dados de uma pessoa específica. **Permite atualizar:** nome, email, data de nascimento.
* **DELETE /pessoas/{id}:** Exclui uma pessoa específica, identificada pelo seu ID.

## Deploy na AWS

A aplicação está hospedada na AWS em uma arquitetura robusta e escalável.

**Arquitetura:**

* **Frontend:** O React frontend é servido através de um S3 bucket e distribuído globalmente pelo CloudFront, garantindo alta performance e disponibilidade.
* **Backend:** O backend Spring Boot é executado em uma instância EC2, autoescalável para atender à demanda.
* **Banco de dados:** O PostgreSQL é gerenciado pelo RDS, proporcionando alta disponibilidade e desempenho.
* **DNS:** O domínio da aplicação é gerenciado pelo Route 53, permitindo um DNS altamente disponível e flexível.

**Processo de deploy:**

1. **Build:** O código-fonte é construído e os artefatos são gerados.
2. **Deploy do frontend:** Os arquivos estáticos do frontend são enviados para o S3 bucket.
3. **Deploy do backend:** A imagem Docker do backend é construída e enviada para o Amazon ECR. Em seguida, um novo serviço ECS é criado ou atualizado para executar a imagem.
4. **Atualização do Load Balancer:** O Load Balancer é atualizado para direcionar o tráfego para o novo serviço ECS.

## Agradecimentos
Agradeço à Simbiose Ventures pela oportunidade de participar deste desafio técnico.

