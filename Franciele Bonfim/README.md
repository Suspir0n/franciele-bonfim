# Site — Franciele Bonfim Fotografia

Site institucional de página única (one-page) para a fotógrafa Franciele Bonfim, especializada em casamentos, eventos religiosos e ensaios infantis em Salvador, BA.

## Estrutura de arquivos

```
index.html                          → o site inteiro (HTML + CSS + JS em um único arquivo)
assets/
  favicon.png                       → ícone da aba do navegador
  logo-icon.jpg                     → monograma "FB" usado no menu e rodapé
  franciele-studio.jpg              → foto de estúdio (hero)
  franciele-hero.png                → foto de rua (seção Sobre)
  franciele-instagram.jpg           → foto usada na seção "Redes sociais"
  portfolio-infantil-1.jpg          → foto real do portfólio (aniversário Príncipe)
  portfolio-infantil-2.jpg          → foto real do portfólio (aniversário Príncipe)
  portfolio-infantil-3.jpg          → foto real do portfólio (ensaio ao ar livre)
  brand/                            → peças separadas do brand board (logo, monograma,
                                       paleta de cores, ícones, cartão de visitas, etc.)
                                       — não são usadas no site, ficam aqui como referência
                                       de identidade visual para outras artes
```

**Importante:** ao mover o site para outro lugar (pendrive, hospedagem, etc.), sempre leve a pasta `assets` inteira junto com o `index.html`. Se faltar algum arquivo dela, a imagem correspondente aparece quebrada.

## Como visualizar

Basta abrir o `index.html` duas vezes clicando nele — abre em qualquer navegador (Chrome, Safari, Edge). Não precisa de servidor nem internet, exceto para carregar a fonte do Google Fonts (Fraunces + Manrope).

## O que já está configurado

- **WhatsApp:** (71) 99112-0774, com mensagem inicial pronta em todos os botões
- **E-mail:** daviibonfim.09@gmail.com
- **Instagram:** @franciele.bf
- **Favicon:** monograma dela na aba do navegador

## O que ainda é placeholder (precisa trocar depois)

1. **Depoimentos** (seção "Depoimentos") — os 3 textos atuais são exemplos escritos por mim pra mostrar o tom. Quando ela tiver depoimentos reais de clientes, trocar o texto dentro de `<p class="msg">` e, se quiser, trocar o ícone `<svg class="t-avatar">` por `<img class="t-avatar" src="assets/foto-do-cliente.jpg">` (o CSS já está pronto pra foto real, com `object-fit:cover`).
2. **Portfólio** — ainda tem blocos coloridos com ícone (casamento/religioso) como placeholder. Basta substituir o `<div class="gallery-item ...">` por uma versão com foto real, no mesmo padrão dos 3 itens que já têm `class="gallery-item has-photo"` com `<img>` dentro.
3. **Galeria privada de entrega de fotos** — o botão "Acessar galeria de fotos" na seção de galeria protegida ainda aponta pra um link vazio (`href="#"`). Quando ela escolher a ferramenta (ex: Pixieset), trocar esse `href` pelo link real ou pelo link de cada evento.
4. **Agenda** — a seção "Agenda" hoje só leva pro WhatsApp. Se no futuro ela quiser um calendário de verdade, dá pra integrar um Google Calendar embutido ali.

## Personalização rápida

Cores, fontes e espaçamento ficam centralizados no início do `<style>`, dentro de `:root`:

```css
:root{
  --cream: #FBF5EE;   /* fundo geral */
  --blush: #F1C8CE;   /* rosa claro */
  --rose-deep: #A94A63; /* rosa escuro (botões, links) */
  --gold: #C9A15A;    /* dourado (detalhes) */
  --lilac: #DCCFEA;   /* lilás (seção galeria privada) */
  --ink: #3B2E2A;     /* texto escuro / fundo do rodapé */
}
```

Trocar qualquer valor aqui muda a cor em todo o site de uma vez.

O espaçamento lateral de todas as seções vem da classe `.container` (padding esquerda 90px / direita 30px, no topo do CSS) — mudar ali afeta o site inteiro de forma consistente.

## Publicar o site (GitHub Pages)

1. Criar um repositório no GitHub e subir o `index.html` e a pasta `assets/` juntos, mantendo a mesma estrutura de pastas
2. Nas configurações do repositório → Pages → escolher a branch `main` e pasta raiz (`/`)
3. O GitHub gera um link tipo `usuario.github.io/nome-do-repo`
4. Se ela tiver domínio próprio (ex: francielebonfim.com.br), configurar como domínio customizado nas mesmas configurações de Pages

## Formulário de contato

O formulário na seção "Contato" não envia e-mail — ele monta uma mensagem e abre o WhatsApp automaticamente com os dados preenchidos. Não precisa de backend nem servidor.
