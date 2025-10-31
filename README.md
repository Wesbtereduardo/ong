# ONG Solidariedade — Aula front-end-web

Site estático de uma ONG com foco em acessibilidade (WCAG 2.1 AA), desenvolvido em HTML, CSS e JavaScript. Inclui páginas de apresentação, projetos e um formulário de cadastro, com navegação e componentes preparados para teclado e leitores de tela.

- Repositório: https://github.com/Wesbtereduardo/ong-solidariedade
- Demonstração (GitHub Pages): https://wesbtereduardo.github.io/ong-solidariedade/

## Sumário

- [Visão Geral](#visão-geral)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Funcionalidades](#funcionalidades)
- [Acessibilidade (WCAG 21 AA)](#acessibilidade-wcag-21-aa)
- [Como Rodar Localmente](#como-rodar-localmente)
- [Deploy (GitHub Pages)](#deploy-github-pages)
- [Padrões de Versionamento](#padrões-de-versionamento)
- [Issues, Milestones e Pull Requests](#issues-milestones-e-pull-requests)
- [Roadmap](#roadmap)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Visão Geral

Este projeto consolida:
- Controle de versão com Git/GitHub, GitFlow simplificado e Commits Semânticos.
- Acessibilidade em conformidade com WCAG 2.1 AA (teclado, ARIA, contraste).
- Documentação técnica com instruções de uso e deploy via GitHub Pages.

## Estrutura do Projeto

```
.
├── index.html
├── projetos.html
├── cadastro.html
├── css/
│   ├── style.css
│   └── cadastro.css
├── js/
│   ├── spa.js
│   ├── projects.js
│   └── cadastro.js
└── assets/
    └── imagens/   (imagens utilizadas no site)
```

- `index.html`: página inicial e navegação.
- `projetos.html`: listagem/descrição de projetos.
- `cadastro.html`: formulário de cadastro.
- `css/style.css`: estilos gerais e temas.
- `css/cadastro.css`: estilos do formulário.
- `js/spa.js`: navegação/comportamentos e acessibilidade do menu.
- `js/projects.js`: lógica de projetos (listagem/dados).
- `js/cadastro.js`: validações/feedback do formulário.

## Funcionalidades

- Navegação com submenu acessível via teclado (Tab/Shift+Tab/Setas/Esc).
- Temas com foco em contraste (claro/escuro/alto contraste).
- Formulário de cadastro com validação e mensagens ao usuário.

## Acessibilidade (WCAG 2.1 AA)

- Teclado:
  - Foco visível com `:focus` e `:focus-visible`.
  - Submenus navegáveis por setas; `Esc` fecha e retorna foco ao botão.
- ARIA:
  - Uso de `aria-label`, `aria-expanded`, `aria-pressed`, `aria-live` quando aplicável.
- Contraste:
  - Paletas de cor visando contraste ≥ 4.5:1.
- Testes sugeridos:
  - Teclado (Tab/Shift+Tab/Enter/Esc/Setas).
  - Lighthouse e Axe DevTools.
  - Leitor de tela (NVDA/VoiceOver).

## Como Rodar Localmente

- Abrir `index.html` diretamente no navegador, ou
- Usar um servidor local (recomendado, ex.: extensão “Live Server” no VS Code).

Passos (Live Server):
1. Abrir a pasta do projeto no VS Code.
2. Instalar a extensão “Live Server”.
3. Clicar em “Go Live” e acessar o endereço indicado (ex.: http://127.0.0.1:5500).

## Deploy (GitHub Pages)

Já publicado (link no topo). Para configurar/ajustar:
1. GitHub Repo → Settings → Pages.
2. Build and deployment → Source: “Deploy from a branch”.
3. Branch: `main` (root).
4. Salvar e aguardar a publicação.
5. URL: `https://<usuario>.github.io/ong-solidariedade/`.

Opcional (Actions): criar um workflow com `actions/upload-pages-artifact` e `actions/deploy-pages`.

## Padrões de Versionamento

- GitFlow (simplificado):
  - `main`: produção.
  - `develop`: integração.
  - `feature/*`: novas funcionalidades.
  - `fix/*`: correções.
  - `hotfix/*`: correções urgentes a partir de `main`.

- Commits Semânticos:
  - `feat: ...` nova funcionalidade
  - `fix: ...` correção de bug
  - `docs: ...` documentação
  - `style: ...` formatação (sem alterar lógica)
  - `refactor: ...` refatoração (sem alterar comportamento)
  - `test: ...` testes
  - `chore: ...` tarefas diversas
  
Exemplos:
- `feat(nav): adiciona submenu acessível com teclado`
- `fix(form): corrige validação de email no cadastro`

## Issues, Milestones e Pull Requests

- Issues:
  - Criar issues para features, bugs e documentação.
  - Usar labels (ex.: `type:feature`, `type:bug`, `docs`, `accessibility`, `deploy`).
  - Referenciar PRs: “Closes #<número>”.

- Milestones:
  - Ex.: “Entrega IV” com escopo e data.
  - Vincular issues à milestone.

- Pull Requests:
  - De `feature/*` para `develop`; e de `develop` para `main`.
  - Descrever objetivo, mudanças e como testar.
  - Vincular issues e milestone.
  - Exigir pelo menos 1 review.

Sugestão de templates (opcional):
- `.github/ISSUE_TEMPLATE/bug_report.md`
- `.github/ISSUE_TEMPLATE/feature_request.md`
- `.github/pull_request_template.md`
- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`

## Roadmap

- Acessibilidade: revisão contínua com ferramentas automáticas.
- Documentação: ampliar exemplos e capturas de tela.
- Otimização (futuro): minificação de HTML/CSS/JS e compressão de imagens.
- CI/CD (futuro): workflow para lint, build e Lighthouse CI.

## Contribuição

1. Criar branch a partir de `develop`:
   - `git checkout -b feature/minha-feature`
2. Commit semântico.
3. Abrir PR para `develop`, descrevendo mudanças e testes.
4. Vincular a uma issue e solicitar revisão.

## Licença

Definir a licença do projeto (ex.: MIT). Caso opte por MIT, crie um arquivo `LICENSE` na raiz com o texto correspondente.

---

## Forma de Entrega (Checklist)

- Repositório público no GitHub com código fonte versionado.
- Histórico de commits organizado com Conventional Commits.
- Pull Requests documentados e revisados.
- Issues e milestones utilizados (ex.: “Entrega IV”).
- README profissional completo na raiz.
- Link público:
  - Repositório: https://github.com/Wesbtereduardo/ong-solidariedade
  - GitHub Pages: https://wesbtereduardo.github.io/ong-solidariedade/
