JavaScript com Node.js: criando sua primeira biblioteca

# 📚 Validador e Processador de Links Markdown (Node.js Library)

Biblioteca desenvolvida durante o curso **"JavaScript com Node.js: criando sua primeira biblioteca"** da Alura. O projeto consiste em uma ferramenta utilitária e CLI (Command Line Interface) capaz de ler arquivos Markdown, extrair links, validar o status de cada um deles e retornar os resultados estruturados.

---

## 🚀 Tecnologias Utilizadas

* **JavaScript (ES6+)**
* **Node.js**
* **CLI (Command Line Interface)**
---

## 🛠️ Funcionalidades e Arquitetura

O projeto foi construído modularmente para separar responsabilidades de leitura, validação e interface:

* **Leitura de Arquivos (`index.js`)**: Processa diretórios e arquivos de texto/Markdown de forma assíncrona utilizando `fs/promises`.
* **Validação de Links (`helpers.js`)**: Faz requisições HTTP para verificar se os links encontrados nos arquivos estão ativos (`200 OK`) ou quebrados.
* **Interface de Linha de Comando (`cli.js`)**: Permite que o usuário interaja com a biblioteca diretamente pelo terminal, passando caminhos de arquivos e acionando validações.
* **Tratamento de Erros (`erros/funcoesErro.js`)**: Mensagens de erro amigáveis e tratadas para falhas comuns (como diretórios inexistentes ou caminhos inválidos).

---

## 📂 Estrutura do Projeto

```text
3709-nodejs-lib-aula-5/
├── arquivos/             # Arquivos Markdown de exemplo para teste
├── resultados/           # Diretório de saída com os resultados gerados
├── src/
│   ├── erros/            # Tratamento de exceções e erros customizados
│   ├── cli.js            # Interface de linha de comando (CLI)
│   ├── helpers.js        # Funções auxiliares (validação de links HTTP)
│   └── index.js          # Ponto de entrada principal da biblioteca
├── package.json          # Dependências e configurações do projeto
└── package-lock.json
