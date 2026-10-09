# Marketplatz

![React Native](https://img.shields.io/badge/React_Native-0.74-61DAFB?logo=react&logoColor=61DAFB)
![CodeIgniter](https://img.shields.io/badge/CodeIgniter-4.5-EF4223?logo=codeigniter&logoColor=EF4223)
![MariaDB](https://img.shields.io/badge/MariaDB-11.4-003545?logo=mariadb&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.0-646CFF?logo=vite&logoColor=646CFF)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.1-38B2AC?logo=tailwind-css&logoColor=38B2AC)
![Inertia.js](https://img.shields.io/badge/Inertia.js-1.0-9553E9?logo=inertia&logoColor=9553E9)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript&logoColor=3178C6)
![Vitest](https://img.shields.io/badge/Vitest-1.6-6E9F18?logo=vitest&logoColor=6E9F18)

<p>Sistema de marketplace para compra e venda de produtos de produtores e artesãos locais.Desenvolvido pelo Municipio de Arabutã
Ajudei na criação do front-end com vue 3 e backend com codeigniter 4.Além disso foi criado um aplicativo mobile com react native (Ainda em testes e ajustes não publicado ). Conexão com API própria. Sistema de autenticação, CRUD completo de produtos, pedidos, pagamentos, avaliações, categorias, marcas, etc.</p>

## Recursos e Destaques

### Experiência de Compra e Marketplace

- **Catálogo e Vitrine Regional**: Busca otimizada e filtros em tempo real por categorias, marcas e produtores e artesãos locais.
- **Carrinho e Gestão de Pedidos**: Fluxo completo de adição/remoção, cálculo dinâmico e atualização de quantidades.
- **Avaliações e Reputação**: Sistema de feedback e notas de produtos e produtores e artesãos locais.
- **Impressão e Relatórios**: Geração e pré-visualização de relatórios e comprovantes para pedidos.

###  Experiência de Venda, PDV e Gestão (Admin & Operador)

- **PDV Físico Integrado (Casa Enxaimel)**: Ponto de venda presencial para comercialização direta dos produtos no ponto turístico cultural, com fechamento ágil de vendas e baixa automática de estoque.
- **Painel e Dashboard Gerencial**: Visão consolidada de métricas, faturamento, produtos mais vendidos e fluxo comercial em tempo real.
- **Perfis de Acesso Diferenciados**: Níveis de permissão e visibilidade isolados para **Administrador** e **Operador**.
- **Gestão Completa de Pedidos (CRUD)**: Acompanhamento de pedidos online e físicos, com controle de status, cancelamentos e entregas.
- **Módulo Financeiro**:
  - **Contas a Receber**: Controle de entradas e recebimentos de vendas no PDV e marketplace.
  - **Contas a Pagar**: Gestão de repasses para produtores e despesas operacionais.
- **Cadastro e Gestão de Vendedores**: Cadastro completo de artesãos e produtores rurais locais com catálogo e dados de repasse.
- **Relatórios Gerenciais e de Vendas**: Emissão e impressão de relatórios de desempenho, histórico financeiro e romaneios de pedidos.


### Aplicativo Mobile (React Native)

- **Multiplataforma (iOS & Android)**: Desenvolvido com React Native e tipagem estrita com TypeScript.
- **Suporte Offline e Cache Local**: Persistência com `AsyncStorage` e monitoramento de conectividade via `NetworkContext`.
- **Tema Claro e Escuro**: Suporte dinâmico a temas claro e escuro (`ThemeContext`).
- **Canal de Atendimento / Chat**: Módulo de comunicação e mensagens integrado ao app.
- **Favoritos e Histórico**: Lista de produtos desejados e acompanhamento de status de pedidos em tempo real.

### Backend, Segurança e API (CodeIgniter 4)

- **Arquitetura em Camadas**: Separação clara entre _Controllers_, _Services_, _Entities_ e _Mappers_.
- **Autenticação e Controle de Acesso**: Middlewares/Filters para proteção de rotas com JWT/Auth e CORS.
- **CRUD Completo e Regras de Negócio**: Gestão unificada de produtos, categorias, marcas, clientes e pagamentos.
- **Banco de Dados Estruturado**: Versionamento com _Migrations_ e povoamento com _Seeds_ em MariaDB/MySQL.

### Engenharia, PWA e Qualidade de Código

- **Experiência PWA (Progressive Web App)**: Service Workers e manifesto web para acesso rápido e instalação no navegador.
- **Pipeline de Testes Automatizados**: Suíte de testes unitários e de integração com **Vitest** (frontend) e **PHPUnit** (backend).
- **Interface Moderna e Responsiva**: Design system com Tailwind CSS e alta performance de compilação via Vite.

## Arquitetura do marketplatz

```text
marketplatz/
├── app/                           # Backend - Código da aplicação (CodeIgniter 4)
│   ├── Config/                    # Configurações do framework e ambiente (App, Database, Routes, etc.)
│   ├── Controllers/               # Camada de controle HTTP/API (entrada de requisições e respostas)
│   ├── Database/                  # Estrutura do banco de dados
│   │   ├── Migrations/            # Versionamento de tabelas e esquemas de dados
│   │   └── Seeds/                 # Povoadores de dados iniciais e de testes
│   ├── Entities/                  # Classes de entidades de domínio (mapeamento objeto-relacional)
│   ├── Filters/                   # Middlewares de requisição (Auth, JWT, CORS, validações)
│   ├── Libraries/                 # Bibliotecas e integrações utilitárias customizadas
│   ├── Mappers/                   # Conversores e formatadores de dados entre camadas
│   ├── Models/                    # Camada de persistência e acesso ao banco de dados (MySQL)
│   ├── Routes/                    # Definições modulares de rotas da aplicação
│   ├── Services/                  # Regras de negócio desacopladas e orquestração de lógica
│   └── Views/                     # Templates e views do backend / relatórios renderizados
│
├── frontend/                      # Frontend - Aplicação SPA modular (Vue 3 + Vite)
│   ├── src/                       # Código-fonte da aplicação Vue
│   │   ├── assets/                # Arquivos estáticos (imagens, ícones, estilos globais CSS)
│   │   ├── components/            # Componentes Vue reutilizáveis (sempre em minúsculas)
│   │   │   ├── cart/              # Componentes de carrinho e checkout
│   │   │   ├── modals/            # Diálogos, popups e modais do sistema
│   │   │   ├── navigation/        # Menus, barras de navegação e cabeçalhos
│   │   │   ├── preview/           # Pré-visualização de imagens e arquivos
│   │   │   ├── print/             # Templates de impressão e relatórios
│   │   │   ├── store/             # Componentes específicos de catálogo e vitrine
│   │   │   └── ui/                # Componentes genéricos de UI (botões, inputs, cards)
│   │   ├── composables/           # Lógica reativa desacoplada (hooks/Composition API)
│   │   ├── constants/             # Constantes globais, status e dicionários de termos
│   │   ├── layouts/               # Layouts estruturais de tela (painel, público, etc.)
│   │   ├── models/                # Interfaces, estruturas de dados e tipagens cliente
│   │   ├── pages/                 # Páginas/Telas principais da aplicação
│   │   ├── services/              # Camada de comunicação com a API (chamadas Axios/Fetch)
│   │   └── utils/                 # Funções puras utilitárias (formatações, moedas, datas)
│   ├── tests/                     # Testes unitários do frontend (Vitest / Vue Test Utils)
│   └── jsconfig.json              # Mapeamento de caminhos e aliases de imports (@/)
│
├── public_html/                   # Raiz web pública (Web Root acessível pelo servidor HTTP)
│   ├── assets/                    # Assets estáticos públicos (CSS, JS legados, imagens públicas)
│   ├── build/                     # Artefatos gerados pelo build do Vite
│   ├── index.php                  # Ponto de entrada (Bootstrap) do CodeIgniter 4
│   └── manifest.json / sw.js      # Recursos e Service Worker para suporte PWA
│
├── scripts/                       # Utilitários, scripts de manutenção e rotinas de automação
│   ├── maintenance/               # Scripts de manutenção e reparo do banco/dados
│   └── setup_xampp.ps1            # Automação de setup de ambiente local
│
├── tests/                         # Testes automatizados do Backend (PHPUnit)
│   ├── _support/                  # Mocks, factories e auxiliares de teste
│   ├── database/                  # Testes de integração de banco de dados
│   └── unit/                      # Testes unitários de Services e regras de negócio
│
├── writable/                      # Diretório de escrita do CI4 (logs, cache, sessões, uploads)
│
├── .env.example                   # Modelo de variáveis de ambiente do projeto
├── composer.json                  # Dependências e scripts do ecossistema PHP
├── package.json                   # Dependências e scripts do ecossistema Node.js / Frontend
├── phpunit.xml.dist               # Configurações de execução de testes PHPUnit
├── spark                          # CLI oficial de comandos do CodeIgniter 4
├── vite.config.mjs                # Configurações do bundler Vite
└── vitest.config.mjs              # Configurações da suíte de testes Vitest

```

## Arquitetura do mobile

```
marketplatz_mobile/
├── App.tsx                        # Componente raiz da aplicação (Providers e inicialização)
├── app.json                       # Configurações do projeto Expo (splash, ícones, plugins)
├── babel.config.js                # Configurações de compilação do Babel
├── metro.config.js                # Configurações do empacotador Metro
├── package.json                   # Dependências e scripts do ecossistema React Native/Expo
├── tsconfig.json                  # Configurações do TypeScript e aliases de path
│
└── src/                           # Código-fonte principal da aplicação móvel
    ├── api/                       # Instância do Axios, interceptors de token e base URL
    ├── assets/                    # Recursos estáticos locais (imagens, ícones e fontes)
    ├── components/                # Componentes reutilizáveis de UI (botões, inputs, cards, headers)
    ├── context/                   # Gerenciamento de estado global via Context API
    │   ├── AuthContext/           # Estado e persistência de sessão do usuário
    │   ├── CartContext/           # Estado do carrinho de compras e checkout
    │   ├── CategoriesContext/     # Estado de categorias de produtos
    │   ├── FavoriteContext/       # Gestão de itens favoritos
    │   ├── NetworkContext/        # Monitoramento de conectividade offline/online
    │   ├── OrderContext/          # Estado de pedidos e histórico
    │   ├── ProductContext/        # Catálogo e listagem de produtos
    │   ├── ThemeContext/          # Alternância e aplicação de temas (claro/escuro)
    │   └── RootProvider.tsx       # Provedor central que encapsula todos os contextos
    ├── database/                  # Persistência local e cache no dispositivo (AsyncStorage)
    ├── helpers/                   # Funções de suporte e validações gerais
    ├── hooks/                     # Custom React Hooks (regras e lógica reativa reutilizável)
    ├── mappers/                   # Conversores e adaptadores de dados da API para o app
    ├── middleware/                # Interceptações de fluxo de dados e regras de acesso
    ├── models/                    # Modelos de domínio e representação de dados
    ├── navigation/                # Estrutura do React Navigation
    │   ├── Navigator/             # Navegadores principais (Bottom Tabs, Drawer, Stacks)
    │   ├── stack/                 # Pilhas de navegação isoladas (AuthStack, AppStack)
    │   ├── RootNavigator.tsx      # Roteador raiz que alterna entre autenticado e visitante
    │   ├── Routes.tsx             # Definição e nomes constantes das rotas
    │   └── types.ts               # Tipagem TypeScript para parâmetros de rotas
    ├── screens/                   # Telas principais organizadas por domínio
    │   ├── auth/                  # Telas de login, cadastro e recuperação de senha
    │   ├── cart/                  # Tela do carrinho e finalização de compra
    │   ├── chat/                  # Telas de mensagens e atendimento
    │   ├── home/                  # Tela inicial, vitrines e banners
    │   ├── order/                 # Detalhes e acompanhamento de pedidos
    │   ├── products/              # Busca, listagem e detalhes do produto
    │   ├── profile/               # Perfil do usuário, endereços e configurações
    │   └── SplashScreen.tsx       # Tela inicial de carregamento/splash
    ├── services/                  # Chamadas de API e integração com backend por entidade
    ├── theme/                     # Tokens de design (paleta de cores, tipografia, espaçamentos)
    ├── types/                     # Tipagens globais do TypeScript
    └── utils/                     # Funções utilitárias (máscaras, formatação de moedas, datas)

```

## Licenciamento & Confidencialidade

> **Nota de Confidencialidade:** Este software foi concebido e implementado sob encomenda institucional. O repositório atua como apresentação técnica e estudo de caso de engenharia de software; o código-fonte proprietário e os binários distribuíveis são de posse exclusiva da entidade promotora.
