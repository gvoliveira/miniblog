#  Miniblog Pessoal com Hugo + GitHub Pages

Este repositório contém o código-fonte de um miniblog pessoal. O projeto foi estruturado para ser construído, configurado e publicado no período de **5 dias**, utilizando o gerador de sites estáticos **Hugo** e a hospedagem gratuita do **GitHub Pages**.

---

##  Visão Geral do Projeto

* **Gerador Estático:** Hugo (Extended)
* **Tema:** PaperMod (ou tema de sua escolha)
* **Hospedagem:** GitHub Pages via GitHub Actions
* **Custo:** R$ 0,00 (Hospedagem e deploy 100% gratuitos)
* **Linguagem do Conteúdo:** Markdown (`.md`)

---

##  Cronograma e Acompanhamento de Etapas (5 Dias)

### [x] Dia 1 — Preparação do Ambiente e Estrutura Inicial
- [ ] Instalar o Hugo Extended e verificar suporte ao Git no terminal.
- [ ] Executar `hugo new site . --force` para inicializar a estrutura do projeto.
- [ ] Inicializar o repositório Git local (`git init`).
- [ ] Escolhar e adicionar o tema como submódulo Git na pasta `/themes`.
- [ ] Configurar o tema no arquivo `hugo.toml`.

### [ ] Dia 2 — Configurações Globais e Paginação
- [ ] Definir o `baseURL`, `languageCode` (pt-br) e título principal no `hugo.toml`.
- [ ] Configurar a paginação (`paginate = 5`) para organizar o feed da página inicial.
- [ ] Personalizar parâmetros do tema (redes sociais, biografia, menu de navegação).
- [ ] Testar o servidor de desenvolvimento local (`hugo server`).

### [ ] Dia 3 — Criação do Primeiro Conteúdo em Markdown
- [ ] Criar a primeira postagem usando o comando `hugo new content posts/primeira-postagem.md`.
- [ ] Configurar o **Frontmatter** do post (`title`, `date`, `draft: false`).
- [ ] Escrever o conteúdo utilizando formatação Markdown (títulos, listas, negrito, blocos de código).
- [ ] Validar a ordenação cronológica e exibição da postagem localmente.

### [ ] Dia 4 — Automação de Deploy com GitHub Actions
- [ ] Criar repositório público no GitHub e vincular ao repositório local.
- [ ] Fazer o *push* dos arquivos para a *branch* principal (`main`).
- [ ] Acessar **Settings > Pages** no GitHub e alterar a fonte de publicação (*Source*) para **GitHub Actions**.
- [ ] Configurar o workflow do Hugo para compilação automática durante os commits.
- [ ] Confirmar o primeiro deploy e verificar se o site está online na URL gerada.

### [ ] Dia 5 — Refinamento, Testes Finais e Documentação
- [ ] Validar a navegação de páginas (paginação) adicionando posts de teste.
- [ ] Testar a responsividade da interface no celular e desktop.
- [ ] Configurar favicon e metadados básicos (SEO).
- [ ] Finalizar a documentação deste `README.md` e realizar a entrega oficial do projeto.

---

##  Como Rodar o Projeto Localmente

Se você deseja clonar este repositório e executar o projeto em sua máquina:

1. **Clonar o repositório (incluindo os submódulos do tema):**
   ```bash
   git clone --recursive [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
   cd nome-do-repositorio
