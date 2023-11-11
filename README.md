## DDD & Clean Architecture

Este projeto utiliza Next.js 14.0.2 seguindo os princípios da Clean Architecture e Domain-Driven Design (DDD) para criar uma aplicação bem estruturada e de fácil manutenção.

Estrutura do Projeto
A estrutura do projeto é organizada de acordo com os conceitos da Clean Architecture, com camadas bem definidas para separar as responsabilidades e facilitar a manutenção e evolução do código.

![alt text](/public/the-clean-architecture.jpg)

### Estrutura de Diretórios

.
├── src
│ ├── app
│ │ ├── layout.tsx
│ │ │── page.tsx
│ │ └── ...
│ ├── core
│ │ ├── entities
│ │ │ ├── ...
│ │ │ └── aggregate-root.ts
│ │ ├── errors
│ │ │ ├── errors
│ │ │ └── use-case-error.ts
│ │ ├── events
│ │ │ ├── ...
│ │ │ │── domain-event.ts
│ │ │ │── domain-events.spec.ts
│ │ │ │── domain-events.ts
│ │ │ └── event-handler.ts
│ │ ├── repositories
│ │ │ ├── ...
│ │ │ └── pagination-params.ts
│ │ ├── types
│ │ │ ├── ...
│ │ │ └── optional.ts
│ │ ├── either.spec.ts
│ │ ├── either.ts
│ ├── domain
│ │ ├── forum
│ │ │ ├── application
│ │ │ │ ├── repositories  
│ │ │ │ └── use-cases
│ │ │ ├── enterprise
│ │ │ │ ├── entities  
│ │ │ │ └── events
│ │ ├── ...
│ │ │ ├── ...
│ │ │ └── ...
│ │ └── ...
│ ├── test
│ │ ├── forum
│ │ │ ├── application
│ │ │ │ ├── repositories  
│ │ │ │ └── use-cases
│ │ │ ├── enterprise
│ │ │ │ ├── entities  
│ │ │ │ └── events
│ │ ├── notification
│ │ │ ├── application
│ │ │ │ ├── repositories  
│ │ │ │ └── use-cases
│ │ │ ├── enterprise
│ │ │ │ ├── entities  
│ │ │ │ └── events
├── public
│ └── images
│ └── clean-architecture.png
├── .gitignore
├── next.config.js
├── package.json
├── README.md
├── next.config.js
├── package.json
├── README.md
└── tsconfig.json

### Descrição dos Diretórios

- core: A pasta core geralmente contém elementos essenciais para o funcionamento do domínio. É onde você - pode encontrar conceitos cruciais que se aplicam diretamente ao núcleo do domínio.
- application: Contém os casos de uso (use cases) da aplicação.
- domain: Representa o núcleo da aplicação, contendo os modelos de domínio e interfaces de repositórios.
- public: Armazena recursos estáticos, como imagens.
