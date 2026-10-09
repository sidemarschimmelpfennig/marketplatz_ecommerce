# Marketplatz E-commerce

![React Native](https://img.shields.io/badge/React_Native-0.74-61DAFB?logo=react&logoColor=61DAFB)
![CodeIgniter](https://img.shields.io/badge/CodeIgniter-4.5-EF4223?logo=codeigniter&logoColor=EF4223)
![MariaDB](https://img.shields.io/badge/MariaDB-11.4-003545?logo=mariadb&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.0-646CFF?logo=vite&logoColor=646CFF)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.1-38B2AC?logo=tailwind-css&logoColor=38B2AC)
![Inertia.js](https://img.shields.io/badge/Inertia.js-1.0-9553E9?logo=inertia&logoColor=9553E9)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript&logoColor=3178C6)
![Vitest](https://img.shields.io/badge/Vitest-1.6-6E9F18?logo=vitest&logoColor=6E9F18)

**Marketplatz** é uma plataforma moderna de e-commerce completa, combinando aplicação mobile em **React Native**, frontend web moderno e ágil com **Vite**, **TypeScript**, **Tailwind CSS** e **Inertia.js**, suportado por um backend robusto em **CodeIgniter** com banco de dados **MariaDB**.

---

## 🚀 Funcionalidades

- **Catálogo Dinâmico de Produtos**: Navegação, busca rápida e filtragem em tempo real.
- **Experiência Multiplataforma**: Aplicação Mobile (React Native) e Web Storefront moderna e responsiva.
- **Integração SPA com Inertia.js**: Comunicação contínua entre o backend CodeIgniter e o frontend moderno sem necessidade de complexidade extra de API REST para as páginas web.
- **Gerenciamento de Carrinho e Pedidos**: Adição, remoção e atualização de itens com cálculo de totais.
- **Backend Robusto e Seguro**: Arquitetura sólida em CodeIgniter com autenticação e validação de regras de negócio.
- **Banco de Dados Confiável**: Persistência estruturada e eficiente em MariaDB.
- **Interface Moderna e Responsiva**: Estilização ágil com Tailwind CSS.
- **Tipagem Estática e Qualidade**: Código limpo e seguro com TypeScript.

---

## 🛠️ Tech Stack

| Camada | Tecnologia | Descrição |
| --- | --- | --- |
| **Mobile** | [React Native](https://reactnative.dev/) | Aplicativo móvel para iOS e Android |
| **Backend** | [CodeIgniter](https://codeigniter.com/) | Framework PHP para lógica de negócio e API |
| **Banco de Dados** | [MariaDB](https://mariadb.org/) | Banco de dados relacional de alta performance |
| **SPA Bridge** | [Inertia.js](https://inertiajs.com/) | Monolito moderno conectando CodeIgniter ao Frontend |
| **Build Tool** | [Vite](https://vitejs.dev/) | Ferramenta de build rápida para o ecossistema frontend |
| **Linguagem Frontend** | [TypeScript](https://www.typescriptlang.org/) | Tipagem estática para maior previsibilidade de código |
| **Estilização** | [Tailwind CSS](https://tailwindcss.com/) | Framework de CSS utilitário para design responsivo |

---

## 📋 Pré-requisitos

Antes de iniciar, certifique-se de ter instalado no seu ambiente:

- [Node.js](https://nodejs.org/) (versão 18.x ou superior)
- [PHP](https://www.php.net/) (versão 8.1 ou superior)
- [Composer](https://getcomposer.org/)
- [MariaDB](https://mariadb.org/) ou MySQL
- Ambiente para React Native configurado (Android Studio / Xcode, JDK)

---

## ⚙️ Instalação e Configuração

### 1. Clonar o repositório

```bash
git clone https://github.com/YourUsername/marketplatz_ecommerce.git
cd marketplatz_ecommerce
```

### 2. Configurar o Backend e Banco de Dados

1. Instale as dependências do PHP:
   ```bash
   composer install
   ```

2. Configure as variáveis de ambiente (`.env` ou `app/Config`):
   ```env
   database.default.hostname = localhost
   database.default.database = marketplatz
   database.default.username = seu_usuario
   database.default.password = sua_senha
   database.default.DBDriver = MySQLi
   database.default.port = 3306
   ```

3. Execute as migrations / crie o banco de dados MariaDB:
   ```bash
   php spark migrate
   ```

### 3. Configurar e Rodar o Frontend Web

1. Instale as dependências do Node:
   ```bash
   npm install
   ```

2. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

### 4. Configurar e Rodar o App Mobile (React Native)

```bash
# Para Android
npm run android

# Para iOS (macOS)
npm run ios
```

---

## 📁 Estrutura do Projeto

```
marketplatz_ecommerce/
├── app/                  # Controladores, Models e Regras de Negócio (CodeIgniter)
├── config/               # Configurações do framework CodeIgniter
├── database/             # Migrations e Seeds (MariaDB)
├── resources/            # Código-fonte Web (Inertia.js + TypeScript + Tailwind)
│   ├── js/
│   │   ├── components/   # Componentes reutilizáveis
│   │   ├── pages/        # Páginas Inertia
│   │   └── types/        # Definições de tipos TypeScript
│   └── css/              # Estilos globais (Tailwind CSS)
├── mobile/               # Aplicação React Native
│   ├── src/
│   │   ├── screens/
│   │   ├── components/
│   │   └── navigation/
│   └── package.json
├── public/               # Ponto de entrada web e arquivos estáticos
├── vite.config.ts        # Configuração do Vite
├── tailwind.config.js    # Configuração do Tailwind CSS
├── tsconfig.json         # Configuração do TypeScript
└── composer.json         # Dependências do backend PHP
```

---

## 🤝 Contribuição

1. Faça um Fork do projeto.
2. Crie uma branch para a sua feature (`git checkout -b feature/NovaFeature`).
3. Faça o commit das suas alterações (`git commit -m 'Adiciona NovaFeature'`).
4. Envie para o branch (`git push origin feature/NovaFeature`).
5. Abra um Pull Request.

---

## 📄 Licença

Este projeto está sob a licença [MIT](LICENSE).