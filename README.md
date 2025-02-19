# Desafio .NET ZEROUM

Agradecemos por demonstrar interesse em tabalhar na ZEROUM Software House!  
A seguir, você encontrará todas as diretrizes necessárias para dar início ao seu teste.

## Recomendações Iniciais

- Leia este documento com atenção e procure seguir todas as instruções à risca;
- Crie um repositório no seu GitHub **sem mencionar nada relacionado à ZEROUM**;
- Registre seus commits diretamente no seu repositório;
- Envie o link do seu repositório para o email **contato@itzeroum.com.br**;
- Você pode utilizar o Google, StackOverflow ou consultar algum projeto pessoal instalado na sua máquina;
- Confira os [Materiais úteis](#materiais-úteis);
- Veja como será a [entrevista técnica](#para-o-dia-da-entrevista-técnica);
- Se tiver qualquer dúvida, sinta-se livre para perguntar aos recrutadores;
- Mantenha a calma e respire fundo – assim como você, nós também já passamos por essa etapa. Boa sorte!

_Corpo do Email com o link do repositório do desafio_

> Seu Nome
>
> Nome do recrutador
>
> Link do repositório
>
> Link do Linkedin

### Sobre o ambiente da aplicação:

Para este teste, você **deverá utilizar o ABP.IO** com as seguintes configurações obrigatórias:

- **Project Type:** Application (Layered)
- **UI Framework:** Angular
- **UI Theme:** LeptonX Lite Theme
- **Database Provider:** EntityFrameworkCore
- **Database Management System:** SQL Server

Siga as boas práticas recomendadas pelo ABP.IO, utilizando toda a estrutura e recursos que o framework oferece. Evite recorrer ao uso excessivo de métodos mágicos ou atalhos prontos, pois queremos avaliar **o seu código** e a forma como você resolve problemas.  

## Para o dia da entrevista técnica

No dia agendado pelo recrutador, certifique-se de que sua aplicação esteja em execução na sua máquina local. Dessa forma, poderemos realizar os testes, analisar os pontos que você desenvolveu e discutir eventuais dúvidas. Durante a entrevista, faremos um code review em conjunto, como se você já fizesse parte do nosso time :heart:. Você terá a oportunidade de explicar suas ideias, detalhar a arquitetura adotada e apresentar propostas de evolução para o projeto.

## Objetivo: Cadastro Simplificado

O Cadastro Simplificado é uma aplicação para gerenciamento de clientes, permitindo a criação, visualização, atualização e exclusão de registros (CRUD). O sistema deve suportar dois tipos de clientes — Pessoa Física e Pessoa Jurídica — e possibilitar a associação de múltiplos endereços para cada cliente.

### Requisitos

#### Cadastro de Clientes

- **Pessoa Física:**  
  - Campos obrigatórios: Nome Completo, CPF, RG, E-mail, Telefone e Data de Nascimento.

- **Pessoa Jurídica:**  
  - Campos obrigatórios: CNPJ, Razão Social, Nome Fantasia, E-mail e Data de Abertura.  
  - Ao informar o CNPJ, os dados relacionados à empresa devem ser obtidos automaticamente através de consulta à API do Receitaws.

- Cada cliente deve ter um identificador único, garantindo que CPF (para pessoas físicas) ou CNPJ (para pessoas jurídicas) não sejam duplicados no sistema.

#### Gestão de Endereços

- Um cliente pode ter vários endereços associados.
- Os endereços devem ser categorizados em três tipos: faturamento, entrega e cobrança. É permitido cadastrar mais de um endereço para cada tipo.
- Ao inserir o CEP, a aplicação deve consultar a API ViaCEP para recuperar automaticamente os dados do endereço (como logradouro, bairro, cidade, etc.), facilitando o cadastro.
- O sistema deve permitir a edição e remoção de endereços já cadastrados.
- O cliente poderá selecionar um endereço de entrega como principal. Esse endereço deverá ser destacado na listagem (grid) junto com as demais informações do cliente.

#### Considerações Técnicas

- A aplicação deve expor uma API RESTful para a manipulação dos clientes e seus endereços.
- As operações de criação, atualização e exclusão devem seguir boas práticas de desenvolvimento, garantindo a integridade dos dados.
- Sinta-se à vontade para propor endpoints ou funcionalidades adicionais que julgar pertinentes, mas procure atender o máximo dos requisitos apresentados.

> Procure ser o mais aderente possível aos requisitos, mas não se preocupe se algum ponto não for completamente implementado. Durante a entrevista, discutiremos o que foi desenvolvido e os desafios enfrentados.

### Endpoints Sugeridos

**Clientes:**

```http request
GET /clients/getAll
POST /clients/createOrEdit
GET /clientes/getByIdForEdit?id={id}
DELETE /clientes/delete?id={id}
```

Caso ache interessante, faça uma proposta de endpoints ou fluxos alternativos e apresente para os entrevistadores :heart:

# Avaliação

Queremos observar como o projeto foi estruturado e desenvolvido tanto no frontend quanto no backend. Procure atender o máximo dos requisitos, mesmo que alguns pontos sejam implementados parcialmente. Durante a avaliação, discutiremos o que foi feito e as áreas que podem ser aprimoradas.

## O que será avaliado e valorizamos :heart:

### Habilidades e Conhecimentos Básicos:
- **Desenvolvimento Backend:** Estruturação de projetos e criação de APIs RESTful.
- **Versionamento:** Uso adequado do Git, com um histórico de commits bem organizado.
- **Capacidade Analítica:** Solução de problemas de forma lógica e estruturada.
- **Código Limpo:** Organização, clareza e facilidade de manutenção.

### Conhecimentos Intermediários e Avançados:
- **Princípios de Desenvolvimento:** Aplicação dos princípios SOLID e identificação de Design Patterns.
- **Documentação:** Clareza na descrição das funcionalidades e na orientação para o uso do projeto.
- **Testes:** Implementação de testes unitários e de integração.
- **Propostas de Melhoria:** Identificação de oportunidades para refatoração e otimização do código.
- **Banco de Dados:** Boas práticas no uso de bancos de dados relacionais.

### Avaliação Específica para ABP.IO e Frontend:
- **Sistema de Permissões:** Utilização eficaz do robusto sistema de permissões do ABP.IO, garantindo que todas as funcionalidades estejam devidamente protegidas.
- **Desenvolvimento Frontend:** Componentização e organização dos componentes em Angular, com foco na reutilização e manutenção.
- **Melhorias na Usabilidade:** Implementação de funcionalidades como paginação, ordenação e filtros nas grids, contribuindo para uma melhor experiência do usuário.

> Nossa avaliação levará em conta a qualidade do código, a organização da solução e a clareza das explicações sobre as decisões tomadas. Durante o processo, vamos conversar sobre os pontos positivos, os desafios encontrados e possíveis melhorias para o projeto.

## O que será um Diferencial

- Uma cobertura de testes consistente
- Documentação
- Proposta de melhoria na arquitetura
- Ser consistente e saber argumentar suas escolhas
- Apresentar soluções que domina
- Modelagem de Dados
- Manutenibilidade do Código
- Tratamento de erros
- Cuidado com itens de segurança
- Arquitetura (estruturar o pensamento antes de escrever)

## Materiais úteis

- https://itzeroum.com.br/
- https://abp.io/
- https://github.com/abpframework/abp
- https://abp.io/docs/latest/
- https://viacep.com.br/
- https://receitaws.com.br/
