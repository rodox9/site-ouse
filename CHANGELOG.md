# Changelog — Site OUSE

Todas as alterações relevantes do site são registradas aqui.
Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) ·
versionamento [SemVer](https://semver.org/lang/pt-BR/).

> Como usar: toda mudança entra primeiro em **[Não publicado]**. Quando publicamos
> (push + tag), move-se o bloco para uma versão com data.

## [Não publicado]
_(nada pendente)_

---

## [1.0.0] — 2026-06-20
Primeiro lançamento. Site institucional no ar em **aouse.com.br** (GitHub Pages).

### Adicionado
- **Home** (`index.html`)
  - Hero "Nascidos dentro do mercado" — números inline, degradê animado, reveal em máscara
  - Origem — narrativa fundadora (2019) + visão 360
  - Problema — "O lead não é ruim, a operação é que não enxerga o caminho"
  - Premissa — "Volume protege · Criativo vence · Primeiro enxergar, depois escalar"
  - Agência tradicional vs. OUSE
  - Serviços — 10 frentes com descritivos
  - Grandes números — +R$4M · +300 mil · +R$500M · 13 anos · 7 anos · SP·PR·SC
  - Faixa de clientes — 10 clientes reais (hover laranja + blur de foco + janela de detalhes)
  - CTA Diagnóstico OUSE
- **Cases** (`cases.html`)
  - Prova real: 5 cases (VKR · A. Gonçalves · Bossa · A3MAIS/Alphaville · Hype INC)
  - Filtros por categoria · cards com número-fantasma em parallax
  - Estudo aprofundado VKR (R$20 mil → R$7 mil) com gráfico de linha animado
  - Antes/Depois com slider arrastável · Diferenciais (padrão OUSE)
- **404** brutalista (`404.html`)
- Sistema: GSAP + ScrollTrigger + Lenis (CDN), cursor custom, loader terminal, reveals
- Deploy: GitHub Pages + domínio `aouse.com.br` + `.nojekyll` + `CNAME`

### Pendências conhecidas
- Formulário/agenda do diagnóstico (CTA hoje aponta para `#`)
- HTTPS — certificado do GitHub em emissão
- Páginas futuras: Método · Sobre/Quem
