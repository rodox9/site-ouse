# Changelog — Site OUSE

Todas as alterações relevantes do site são registradas aqui.
Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) ·
versionamento [SemVer](https://semver.org/lang/pt-BR/).

> Como usar: toda mudança entra primeiro em **[Não publicado]**. Quando publicamos
> (push + tag), move-se o bloco para uma versão com data.

## [Não publicado]
### Adicionado (aguardando chaves para ativar → vira v1.2.0)
- Diagnóstico — integração de notificações no envio: **e-mail (Web3Forms)** + **WhatsApp (CallMeBot)**, com resumo formatado do lead. Falta preencher `WEB3FORMS_KEY` e `WHATSAPP_PHONE`/`WHATSAPP_APIKEY` em `diagnostico.html`.

---

## [1.1.1] — 2026-06-20
### Alterado
- Diagnóstico — **WhatsApp** com máscara BR `(00) 00000-0000` + teclado numérico; **e-mail** com validação e teclado de e-mail; `inputmode`/`autocomplete` em todos os campos
- **Q5** ("cenário") virou múltipla escolha (checkbox), texto ajustado para "Quais cenários descrevem o momento atual?"
- **Q10** simplificada: "Você sabe em quanto tempo seu lead é atendido?" → Sim, tenho controle / Não, não tenho controle
- **Q12** (indicadores) e **Q13** (prioridade) reduzidas para 5 opções principais e lógicas

---

## [1.1.0] — 2026-06-20
### Adicionado
- **Página Diagnóstico** (`diagnostico.html`) — "Leitura da Operação Imobiliária"
  - Experiência multi-etapas: **7 etapas visuais, 14 perguntas** (identificação · perfil · momento · demanda · leads · gestão · prioridade)
  - Painel-mapa que preenche conforme avança · barra de progresso · transições com motion · validação por etapa
  - Tela de sucesso personalizada (nome + dor/prioridade apontadas pelo lead)
  - Captura de lead pronta para integração via `SUBMIT_ENDPOINT` (Formspree/webhook)

### Alterado
- CTAs "Diagnóstico OUSE" (nav, seção e rodapé — Home e Cases) agora apontam para `diagnostico.html`

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
