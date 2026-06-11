# Letícia Dala — Landing Page

Site estático (HTML + CSS puro, **sem JavaScript e sem build**) recriado a partir do
site original feito em WordPress/Elementor. Carrega rápido e pode ser hospedado de graça.

## Estrutura

```
site/
├── index.html          # a página inteira (header + conteúdo + footer)
├── css/
│   └── styles.css      # todo o estilo
└── assets/
    ├── hero.jpg            # foto principal
    ├── leticia-2.jpg       # segunda foto
    ├── logo.png            # logotipo vertical (bege)
    ├── logo-horizontal.png # logotipo horizontal (bege)
    ├── logo-branco.png     # logotipo horizontal branco (usado no header)
    └── favicon.png         # ícone da aba do navegador
```

> O header tem o menu (Abordagem / Sobre mim / Contato) que rola até as seções
> da página, e no celular vira menu hamburguer **sem JavaScript** (só CSS).
> O footer tem os contatos (WhatsApp, telefone, Instagram e e-mail).

## Ver localmente

Abra o `index.html` direto no navegador, **ou** rode um servidor simples:

```powershell
py -m http.server 5500 --directory .
# depois acesse http://localhost:5500
```

## Publicar no GitHub Pages

1. Crie um repositório no GitHub e suba o **conteúdo desta pasta `site/`** na raiz
   (ou seja: `index.html` deve ficar na raiz do repositório).
2. No repositório: **Settings → Pages → Branch: `main` / `/root` → Save**.
3. Em ~1 min o site fica no ar em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

### Domínio próprio (leticiadalapsicologa.com)

1. Em **Settings → Pages → Custom domain**, digite `leticiadalapsicologa.com` e salve
   (isso cria um arquivo `CNAME` no repo).
2. No painel de DNS do domínio (na Hostinger), aponte para o GitHub Pages:
   - 4 registros **A** para `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - 1 registro **CNAME** de `www` para `SEU-USUARIO.github.io`
3. Marque **Enforce HTTPS** depois que o DNS propagar.

> Dica: outras hospedagens estáticas gratuitas (Netlify, Cloudflare Pages, Vercel)
> também funcionam — é só arrastar a pasta.

## Editar

- **Textos:** edite direto no `index.html`.
- **Número do WhatsApp:** procure por `wa.me/5583993286060` no `index.html`
  (aparece em 4 lugares: ícone do header, botão do hero, botão "Converse comigo
  agora!" e botão "Fale comigo agora" do footer).
- **Telefone / Instagram / e-mail:** ficam no footer — procure por `tel:`,
  `instagram.com/psi.leticiadala` e `mailto:` no `index.html`.
- **Cores/tamanhos:** ficam todos no topo do `css/styles.css` (variáveis `--bege`,
  `--creme`, `--destaque`, `--rosa`).
- **Imagens:** substitua os arquivos em `assets/` mantendo os mesmos nomes.
