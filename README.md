# blog Pessoal

> Blog pessoal do **Prof. Gilberto** — um espaço para compartilhar ideias,
> materiais didáticos e reflexões sobre tecnologia, educação e programação.

[![Deploy](https://github.com/gvoliveira/miniblog/actions/workflows/hugo.yaml/badge.svg)](https://github.com/gvoliveira/miniblog/actions/workflows/hugo.yaml)
[![Hugo](https://img.shields.io/badge/Hugo-0.167-FF4088?logo=hugo&logoColor=white)](https://gohugo.io/)
[![Theme](https://img.shields.io/badge/Theme-LoveIt-blue)](https://github.com/dillonzq/LoveIt)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](./LICENSE)

---


## Sobre o projeto

Este é um blog estático construído com **Hugo** e hospedado gratuitamente
no **GitHub Pages**. O objetivo é ter um espaço próprio, leve e de fácil
manutenção, para publicar textos sem depender de plataformas terceiras.

O repositório é **público** por dois motivos: serve como portfólio técnico
e permite que outros professores e estudantes aprendam com a estrutura.
O **conteúdo dos posts**, porém, é protegido por direitos autorais — veja
a seção [Licença](#-licença) para detalhes.

### Características

- **Build ultrarrápido** — menos de 100ms por build completo
- **Tema LoveIt** — responsivo, com dark mode e suporte a múltiplos idiomas
- **Deploy automático** — GitHub Actions compila e publica a cada push
- **SEO otimizado** — meta tags, Open Graph e sitemap automáticos
- **Mobile-first** — layout adaptado para leitura em qualquer tela

---

## Stack

| Camada | Tecnologia |
|---|---|
| Gerador estático | [Hugo Extended](https://gohugo.io/) v0.167+ |
| Tema | [LoveIt](https://github.com/dillonzq/LoveIt) |
| Hospedagem | [GitHub Pages](https://pages.github.com/) |
| CI/CD | [GitHub Actions](https://github.com/features/actions) |
| Conteúdo | Markdown |
| Ícones | Font Awesome 5 |

---

## Estrutura do projeto

```
miniblog/
├── .github/
│   └── workflows/          # Pipeline de deploy automático
├── archetypes/             # Templates para novos posts
├── assets/                 # SCSS, JS e recursos processados
│   ├── css/
│   └── jsconfig.json
├── content/                # Conteúdo em Markdown
│   ├── posts/              # Posts do blog (Page Bundles)
│   └── sobre/              # Página "Sobre"
├── data/                   # Dados estruturados (YAML/JSON)
├── layouts/                # Overrides de templates do tema
│   └── _partials/
│       └── head/
│           └── link.html   # Customização do favicon
├── static/                 # Arquivos estáticos servidos na raiz
│   ├── avatar.png
│   └── favicon.ico
├── themes/
│   └── LoveIt/             # Tema (submódulo Git)
├── .gitignore
├── .gitmodules
├── hugo.toml               # Configuração principal
└── README.md
```

---

## Como rodar localmente

### Pré-requisitos

- [Hugo Extended](https://gohugo.io/installation/) v0.158+ (para suportar `locale`)
- [Git](https://git-scm.com/) com suporte a submódulos

### Passo a passo

```bash
# 1. Clone o repositório com os submódulos (o tema é um submódulo Git)
git clone --recursive https://github.com/gvoliveira/miniblog.git
cd miniblog

# 2. Se já clonou sem --recursive, inicialize o submódulo
git submodule update --init --recursive

# 3. Inicie o servidor de desenvolvimento
hugo server --disableFastRender
```

O site estará disponível em: **http://localhost:1313/miniblog/**

### Build de produção

```bash
hugo --gc --minify
```

Os arquivos finais ficam em `public/` (ignorado pelo Git).

---

## Como escrever um novo post

### Usando Page Bundle (recomendado)

```bash
hugo new content posts/meu-novo-post/index.md
```

Isso cria:

```
content/posts/meu-novo-post/
├── index.md
└── (coloque aqui as imagens do post)
```

Depois edite o `index.md`, ajuste o front matter e escreva em Markdown.

### Front matter recomendado

```yaml
---
title: "Título do post"
date: 2026-10-02
draft: false
description: "Uma frase que resume o post (usada no SEO)."
tags: ["hugo", "git"]
categories: ["Tutoriais"]
lightgallery: true
---
```

### Inserindo imagens

Coloque a imagem na mesma pasta do `index.md` e use o shortcode:

```markdown
{{< figure src="minha-imagem.png" alt="Descrição" caption="Legenda" >}}
```

---

## Como publicar

O deploy é **automático**. A cada push na branch `main`:

1. O GitHub Actions dispara o workflow `.github/workflows/hugo.yaml`
2. O Hugo compila o site
3. O resultado é publicado no GitHub Pages

**Para publicar uma mudança:**

```bash
git add .
git commit -m "feat: novo post sobre X"
git push
```

Aguarde ~1 minuto e acesse o site publicado.

---

## Roadmap

- [x] Estrutura inicial com Hugo + LoveIt
- [x] Deploy automático via GitHub Actions
- [x] Favicon customizado
- [x] Ícones sociais (GitHub, LinkedIn, Lattes)
- [x] Limpeza do repositório (`.gitignore`)
- [ ] Primeiros posts autorais
- [ ] Página "Sobre" completa
- [ ] Integração com comentários (Giscus)
- [ ] Analytics (Plausible)
- [ ] Busca local

---

## Licença

Este projeto tem **duas licenças distintas**, dependendo do que está sendo usado:

### Código

Todo o **código-fonte** (templates, configurações, scripts, arquivos CSS/JS
customizados) está licenciado sob a **MIT License** — veja o arquivo
[LICENSE](./LICENSE) para detalhes.

Você pode livremente usar, modificar e distribuir o código, desde que
mantenha o aviso de copyright original.

### Conteúdo

Todo o **conteúdo editorial** (textos dos posts, imagens autorais, materiais
didáticos) é de propriedade do autor:

> © 2022–2026 Prof. Gilberto. Todos os direitos reservados.
>
> A reprodução parcial é permitida **apenas** com atribuição clara e link
> para o texto original. A reprodução integral, o uso comercial ou a
> republicação sem autorização expressa **não são permitidos**.

Para pedidos de uso, entre em contato via [GitHub](https://github.com/gvoliveira).

---

## Créditos

- Tema: [LoveIt](https://github.com/dillonzq/LoveIt) por Dillon
- Gerador: [Hugo](https://gohugo.io/)
- Hospedagem: [GitHub Pages](https://pages.github.com/)

---

<p align="center">
  Feito com ☕ e Markdown por <a href="https://github.com/gvoliveira">Prof. Gilberto</a>
</p>