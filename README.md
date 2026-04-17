# Portfólio · Regiane Pereira

Site estático (HTML + CSS, sem build). Pronto para deploy em GitHub Pages, Vercel, Netlify, Cloudflare Pages ou qualquer host estático.

## Estrutura

```
portfolio/
├── index.html       ← página única, CSS embutido
└── assets/
    ├── foto-regiane.png
    ├── labirinto.png
    ├── tattoo.png
    ├── urbano.png
    ├── cachorros.png
    └── assinatura.png
```

## Decisões de design

- **Paleta:** Grafite Carvão `#1C1916` (fundo), Papel Antigo `#E8DDC9` (texto), Bordô `#8B1E2B` (etiquetas de frente + LinkedIn), Ocre `#C89B4C` (itálicos + STAR markers + WhatsApp)
- **Tipografia:** Instrument Serif (títulos editoriais) + Geist Sans (corpo) + Geist Mono (eyebrows e labels)
- **Textura:** Noise SVG embutido em CSS, blend overlay. Vignette radial aquecida nas bordas.
- **STAR markers:** `●` Situação · `◎` Tarefa · `▶` Ação · `■` Resultado

## Responsivo

Testado em 390px (mobile portrait) e 1440px (desktop). Breakpoints principais: 680px (camadas), 720px (princípios), 820px (bento de cases), 900px (além da fintech), 1100px (princípios em 4 colunas).

## Três pontos pendentes (marcados `data-todo` no HTML)

1. **LinkedIn** — colocar URL real no primeiro botão do bloco `.cta-actions`
2. **WhatsApp** — colocar link `wa.me/55...` no segundo botão
3. **PDF** — hospedar o `Portfolio_Externo_Regiane.docx` (exportado como PDF) e linkar no terceiro botão

Para encontrar e trocar, busque no HTML: `data-todo=`

## Deploy rápido

**GitHub Pages:** suba os arquivos num repositório público, ative Pages em Settings → Pages → main branch → root.

**Vercel / Netlify:** arraste a pasta inteira na interface de drop.

**Cloudflare Pages:** conecta ao repositório git, sem build command necessário.

## Ajustes fáceis de fazer

- **Trocar métricas destaque:** procurar por `.metric` dentro de cada `.case-card`
- **Trocar texto dos cases:** cada case é um `<article class="case-card">` com as 4 etapas STAR marcadas por `.step`
- **Acrescentar um case:** copiar um `.case-card` existente, ajustar `size-wide` / `size-std` / `size-half` conforme a largura desejada (grid de 6 colunas)
- **Remover seção "Além da Fintech":** apagar `<section class="beyond" id="alem">` e o link correspondente no `<nav>`

## Créditos técnicos

- Fontes: Google Fonts (Instrument Serif, Geist, Geist Mono) — carregadas via `<link>` no `<head>`
- Nenhuma dependência JavaScript
- Acessibilidade: contraste AA verificado no corpo de texto, `prefers-reduced-motion` respeitado, `aria-label` nos botões de contato
