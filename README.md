# Pedro AdeA — Portfólio

Site de portfólio de um arquivo só (`index.html`), sem build, sem dependências pesadas.
Vermelho e preto, fundo com blur, grid 2x2 de vídeos e seção de contato.

## Como abrir

Dá um duplo clique no `index.html` e ele abre direto no navegador. Pra publicar
de verdade, veja "Colocar no ar" mais abaixo.

## O que já está pronto

- Nome "Pedro AdeA" no topo e como título principal.
- Grid 2x2 com 4 formatos: Vertical, VSL, Ad Full AI, Vídeo longo.
- Contatos já preenchidos:
  - Discord (abre o perfil pelo ID `643206026304290857`)
  - Email (`pedroandradedeabreu@gmail.com`)
  - WhatsApp (`5561985897900`, com link `wa.me` já pronto pra abrir conversa)
  - Twitter/X — **falta seu usuário**, veja abaixo.

## O que você precisa trocar

### 1. Imagem de fundo
Você pediu pra usar uma imagem específica, mas ela não veio anexada na mensagem.
Por enquanto o fundo é um gradiente vermelho/preto gerado com CSS (com blur e uma
textura bem sutil, só pra não ficar chapado).

Pra colocar sua imagem real, abra `index.html`, procure o bloco `.bg-layer` no
`<style>` e troque:

```css
.bg-layer{
  background-image: url('sua-imagem.jpg');
  /* apague as linhas de gradient/radial que estão logo abaixo */
}
```

Coloque o arquivo de imagem na mesma pasta do `index.html`. O blur (`filter: blur(38px)`)
já está configurado — não precisa mexer nele, só na imagem.

### 2. Vídeos
Cada card em `.grid-2x2` tem uma tag `<video>` com `src=""` vazio. Troque pelo
link do seu vídeo (arquivo `.mp4` hospedado em algum lugar, ou um link direto):

```html
<source src="videos/vertical-01.mp4" type="video/mp4">
```

Se preferir usar YouTube/Vimeo em vez de arquivo direto, troque o `<video>` por
um `<iframe>` do player deles — me chama que eu ajusto isso pra você se quiser.

### 3. Twitter/X
Procure `SEU_USUARIO` (aparece duas vezes, no `href` e no texto) e troque pelo
seu @ de verdade.

## Colocar no ar

Formas simples e gratuitas:

- **GitHub Pages**: cria um repositório, sobe o `index.html`, ativa Pages nas
  configurações do repo.
- **Netlify / Vercel**: arrasta a pasta inteira no site deles (drag and drop),
  eles geram o link na hora.

Qualquer uma das duas funciona sem precisar mexer em código de servidor.

## Sobre a performance

O site não usa JavaScript pesado, não tem parallax nem animação constante —
só o blur do fundo (que é leve, é uma imagem estática desfocada, não
recalculada a cada frame) e uma transição simples no hover dos links/cards.
Isso foi proposital, pra manter fluido mesmo em celular.
