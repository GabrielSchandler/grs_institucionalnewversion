# GRS Soluções — Site institucional (versão estática)

Versão em HTML, CSS e JavaScript puro do site da GRS Soluções.
Plain HTML/CSS/JavaScript version of the GRS Soluções website.

[🇧🇷 Português](#-português) · [🇺🇸 English](#-english)

---

## 🇧🇷 Português

### Sobre o projeto

Página única (one-page) da GRS Soluções, empresa especializada em revisão de juros abusivos e de contratos bancários. O site apresenta a empresa, os serviços e as avaliações de clientes, e leva o visitante a uma consulta gratuita pelo WhatsApp.

> ℹ️ O site oficial hoje roda no repositório [`grs_institucional`](https://github.com/GabrielSchandler/grs_institucional), em Next.js. Este repositório guarda a versão estática anterior.

**Destaques:**
- Seções: início, sobre nós, serviços, avaliações e contato, com botão de WhatsApp.
- Contato pelo WhatsApp em todas as chamadas para ação.
- `apps-script.gs`: endpoint do Google Apps Script que grava leads numa planilha. Ele está pronto no repositório, mas a página atual não o utiliza (o contato é feito pelo WhatsApp).
- SEO básico: `sitemap.xml`, `robots.txt`, `site.webmanifest`, favicons e imagem de compartilhamento (Open Graph).

### Tecnologias

- HTML5, CSS3 e JavaScript puro (sem framework e sem build)
- Google Apps Script (endpoint de leads, opcional)
- GitHub Pages com domínio próprio (`CNAME`)

### Como rodar localmente

Abra o `index.html` no navegador ou suba um servidor simples na pasta:

```bash
python -m http.server 8000   # http://localhost:8000
```

### Endpoint de leads (opcional)

Para gravar leads numa planilha:

1. Na planilha, abra **Extensões > Apps Script** e cole o conteúdo de `apps-script.gs`.
2. Em **Propriedades do script**, configure `SPREADSHEET_ID`, `SHEET_NAME` e `WEBHOOK_SECRET`.
3. Publique como **Web App** e envie os dados (com o `secret`) para a URL `/exec`.

### Estrutura

```
index.html        página completa
styles.css        estilos
script.js         animações e interações da página
apps-script.gs    endpoint opcional do Google Apps Script para gravar leads
favicon*, og-image.png, site.webmanifest, robots.txt, sitemap.xml
```

---

## 🇺🇸 English

### About

A one-page website for GRS Soluções, a company that reviews abusive interest rates and bank contracts. It presents the company, its services and client reviews, and leads visitors to a free consultation on WhatsApp.

> ℹ️ The official website now lives in the [`grs_institucional`](https://github.com/GabrielSchandler/grs_institucional) repository (Next.js). This repository keeps the earlier static version.

**Highlights:**
- Sections: hero, about us, services, reviews and contact, with a WhatsApp button.
- WhatsApp contact on every call-to-action.
- `apps-script.gs`: a Google Apps Script endpoint that writes leads to a spreadsheet. It ships with the repo, but the current page doesn't use it (contact goes through WhatsApp).
- Basic SEO: `sitemap.xml`, `robots.txt`, `site.webmanifest`, favicons and an Open Graph share image.

### Tech stack

- HTML5, CSS3 and vanilla JavaScript (no framework, no build step)
- Google Apps Script (optional lead endpoint)
- GitHub Pages with a custom domain (`CNAME`)

### Running locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000   # http://localhost:8000
```

### Lead endpoint (optional)

To store leads in a spreadsheet:

1. In the sheet, open **Extensions > Apps Script** and paste the contents of `apps-script.gs`.
2. Under **Script properties**, set `SPREADSHEET_ID`, `SHEET_NAME` and `WEBHOOK_SECRET`.
3. Deploy it as a **Web App** and POST the data (with the `secret`) to the `/exec` URL.

### Project structure

```
index.html        the whole page
styles.css        styles
script.js         page animations and interactions
apps-script.gs    optional Google Apps Script lead endpoint
favicon*, og-image.png, site.webmanifest, robots.txt, sitemap.xml
```
