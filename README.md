# OUSE — Site Institucional

Marketing imobiliário 360. Site estático (HTML/CSS/JS) com GSAP + Lenis via CDN. Sem build.

- **Live:** https://aouse.com.br
- **Repo:** github.com/rodox9/site-ouse · branch `main` · GitHub Pages (raiz)

## Páginas
| Arquivo | Página |
|---|---|
| `index.html` | Home — manifesto, origem, problema, premissa, serviços, números, clientes, diagnóstico |
| `cases.html` | Cases — prova real OUSE, estudo VKR, antes/depois, diferenciais |
| `404.html` | Página de erro |

---

# 🏛️ Governança

## 1. Versionamento (SemVer)
`MAIOR.MENOR.CORREÇÃO` — ex.: `1.2.0`

| Sobe | Quando |
|---|---|
| **MAIOR** (2.0.0) | Redesign / reestruturação grande → vira nova pasta `output/v{N}` no projeto OPENSQUAD |
| **MENOR** (1.1.0) | Nova seção ou página |
| **CORREÇÃO** (1.0.1) | Ajuste de conteúdo, copy, bug, layout |

Cada release recebe uma **tag git** (`v1.0.0`) e um **GitHub Release**.

## 2. Changelog
Toda alteração é registrada no [`CHANGELOG.md`](CHANGELOG.md).
Mudança nova entra em **[Não publicado]**; ao publicar, vira um bloco de versão com data.

## 3. Convenção de commits
`tipo: descrição curta no imperativo`

| Tipo | Uso |
|---|---|
| `feat:` | nova seção/funcionalidade |
| `content:` | mudança de texto, copy ou dados |
| `fix:` | correção (bug, scroll, layout) |
| `style:` | ajuste visual sem mudar conteúdo |
| `deploy:` | publicação / infra (DNS, Pages, CNAME) |
| `docs:` | documentação (changelog, readme) |
| `chore:` | manutenção |

Todo commit termina com:
```
Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>
```

## 4. Fluxo de trabalho (sempre nesta ordem)
1. Edita os arquivos em `codigo/`
2. Anota a mudança no `CHANGELOG.md` (bloco **[Não publicado]**)
3. `git commit` seguindo a convenção
4. `git push` (publica no Pages em ~1 min)
5. Se mudou o visual → regera as lâminas: `node ../_shots.cjs`
6. Ao fechar uma versão → move o changelog, cria tag + release:
   ```
   git tag v1.1.0 && git push --tags
   gh release create v1.1.0 --notes-from-tag
   ```

## 5. Boas práticas
- **Nunca** force-push sobre `main` depois do lançamento (só em emergência).
- **Backup:** o repo no GitHub é a fonte da verdade — não depende da pasta local.
- **Lâminas** (`../laminas/`) são geradas, não editadas à mão — sempre via `_shots.cjs`.
- **Dados reais** (clientes/cases) só entram com autorização para apresentação comercial.
- Mexer no sistema de agentes/marcas da OPENSQUAD é via `/opensquad`, não na mão.

Fonte do projeto: OPENSQUAD · `brands/ouse/projetos/site-institucional-2026`.
