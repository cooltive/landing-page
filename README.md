# Cooltive Landing Page

Landing page estática em **HTML + TailwindCSS (CDN)** para divulgação do app de gerenciamento de cultivo **Cooltive**.

## Estrutura
```
landing-page/
  assets/
    icon.png
  index.html
  README.md
```

## Seções Incluídas
- Navbar fixa com CTA de download
- Hero com proposta de valor
- Recursos (features)
- Benefícios + Tabela comparativa Free vs PRO
- Preços (R$30/mês PRO)
- Depoimentos
- FAQ
- CTA final
- Footer

## Cores
Foi usada uma paleta agrícola (verde primário + amarelo/acento) definida diretamente na configuração Tailwind (inline) em `index.html`:
```js
colors: {
  primary: { 50:'#f2fbea',100:'#e3f6d1',200:'#c5eaa3',300:'#a7de75',400:'#89d247',500:'#6cc71a',600:'#56a80f',700:'#43810c',800:'#2e5908',900:'#1d3904'},
  accent:  { 50:'#fff9eb',100:'#ffeec6',200:'#ffdd8d',300:'#ffcb55',400:'#ffba1c',500:'#e6a100',600:'#b37900',700:'#805200',800:'#4e2d00',900:'#261600'}
}
```
Se quiser alterar conforme as cores reais do `icon.png`, ajuste manualmente essas escalas ou substitua apenas `primary.500` e `accent.400` e gere variações mais claras/escuras (pode usar ferramentas como coolors.co ou tailwindcolorshades).

## Alterar link da Play Store
Procure por `https://play.google.com/store/apps/details?id=com.cooltive` dentro do `index.html` e substitua se necessário.

## Deploy Rápido
Como é totalmente estático:
- GitHub Pages: colocar repositório e apontar para branch principal.
- Vercel / Netlify: arraste a pasta ou conecte o repositório (não há build step).
- Nginx / Apache: servir diretamente o `index.html` e pasta `assets`.

## SEO & Metadados
Metatags básicas adicionadas (title, description, keywords, Open Graph e Twitter card). Ajuste conforme critérios de ASO/SEO.

## Acessibilidade
- Hierarquia de headings preservada.
- Botões com foco visível (`focus:ring`).
- Imagens com `alt`.

## Possíveis Melhorias Futuras
- Extração automática da paleta do `icon.png` via Canvas e ajuste dinâmico de variáveis CSS.
- Dark/Light toggle (hoje somente dark).
- Animações sutis de scroll (IntersectionObserver).
- Componente de formulário de captura de e-mail (newsletter / waitlist).

## Como adicionar um formulário simples (exemplo rápido)
Inserir antes da seção FAQ:
```html
<section class="py-24">
  <div class="max-w-xl mx-auto px-4 text-center">
    <h2 class="text-2xl font-semibold">Receba novidades</h2>
    <p class="text-neutral-400 mt-2 text-sm">Lançamentos de novos recursos e dicas de cultivo.</p>
    <form class="mt-6 flex flex-col sm:flex-row gap-3">
      <input type="email" required placeholder="Seu e-mail" class="flex-1 px-4 py-3 rounded-lg bg-neutral-900 border border-neutral-700 focus:outline-none focus:ring-2 focus:ring-primary-400/50" />
      <button class="px-6 py-3 rounded-lg bg-primary-500 hover:bg-primary-400 text-neutral-900 font-medium text-sm">Inscrever</button>
    </form>
  </div>
</section>
```

## Licença
Uso interno do projeto. Defina uma licença pública (MIT / Apache-2.0) se for abrir o código.

---
Feito com foco em velocidade de publicação e clareza da oferta do produto.
