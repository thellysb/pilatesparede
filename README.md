# 🧘‍♀️ Clone Estrutura Completa - Quiz Pilates na Parede

Clone 100% funcional, independente e pronto para produção do funil **Pilates na Parede** (`quiz.pilatespro.site`), totalmente livre de travas de domínio da Inlead/Web2Wave.

---

## 📁 Estrutura de Arquivos

```
pilates-quiz-clone/
├── index.html                  # Página principal do Quiz/Funil (Next.js desvinculado e destravado)
├── README.md                   # Este guia de instalação e configuração
├── _next/                      # Todos os scripts, estilos e fontes estáticos locais
│   └── static/
│       ├── chunks/             # Chunks JavaScript locais (com patch de domínio)
│       ├── css/                # Folhas de estilo Tailwind e animações
│       └── media/              # Fontes locais (Inter, Sora, Montserrat)
└── assets/
    ├── images/                 # Todas as 71 imagens originais do funil salvas localmente
    └── image_map.json          # Mapeamento completo das imagens originais x locais
```

---

## 🚀 Como Subir no Seu Novo Domínio

Você pode hospedar este funil em **qualquer serviço de hospedagem web**, sem necessidade de instalar Node.js ou compilar nada:

### Opção 1: cPanel / Hostinger / Hospedagem Compartilhada
1. Acesse o **Gerenciador de Arquivos** da sua hospedagem.
2. Navegue até a pasta raiz do seu domínio ou subdomínio (geralmente `public_html/` ou `quiz.seudominio.com/`).
3. Envie todos os arquivos e pastas da pasta `pilates-quiz-clone`:
   - `index.html`
   - pasta `_next` (com todo o conteúdo)
   - pasta `assets`
4. Acesse seu domínio pelo navegador: o quiz abrirá imediatamente!

### Opção 2: Vercel / Netlify / Cloudflare Pages
1. Crie um novo projeto estático.
2. Aponte a raiz do projeto para a pasta `pilates-quiz-clone`.
3. Defina o comando de build como vazio (pois já está 100% estático).
4. O deploy será concluído em menos de 1 minuto!

---

## 🎯 Configuração de Checkout

Para facilitar ao máximo, adicionamos um controle direto no topo do arquivo `index.html`:

Abra o arquivo [index.html](file:///C:/Users/GAMER%20-%20PC/.gemini/antigravity/scratch/pilates-quiz-clone/index.html) e localize as primeiras linhas do `<head>`:

```javascript
// =======================================================================
// CONFIGURAÇÃO DE CHECKOUT
// =======================================================================
window.CHECKOUT_URL = null; // Exemplo: "https://go.centerpag.com/PPU38CQH40M"
```

- **Se deixar `null`**: O botão da etapa final direcionará para o link original (`https://wvltrack.com/t/obqtdteste`).
- **Se colocar o seu link**: Basta colar a URL do seu checkout entre aspas (ex: `window.CHECKOUT_URL = "https://go.centerpag.com/PPU38CQH40M";`).
- **Rastreamento Automático**: O motor da página preserva e repassa automaticamente todos os parâmetros de UTMs da URL do lead para o checkout!

---

## 📊 Rastreamento & Pixels Integrados

O clone já vem com:
1. **Utmify**: Script oficial atualizado já configurado no cabeçalho do `index.html`.
2. **Meta Ads Pixel (Facebook)**: Pixels já declarados prontos para registrar `PageView` e eventos de funil.
3. **TikTok Pixel**: Estrutura pronta para campanhas no TikTok Ads.

---

## 🔒 O Que Foi Destravado?

1. **Bypass de Domínio Inlead**: O verificador proprietário (`t == ec.domain`) foi desativado no chunk `70165-eb91bfdeece8be62.js`. O React agora monta normalmente em qualquer domínio, subdomínio ou porta local.
2. **Independência de CDN**: Todas as dependências `_next` foram baixadas para a pasta local, evitando que uma eventual queda ou bloqueio do servidor original afete sua página.
3. **Imagens Preservadas**: Todas as 71 imagens, gráficos comparativos de antes/depois e ilustrações anatômicas foram arquivadas localmente em `assets/images/`.
