# Closet Thay & Lú - Site de Fidelidade

Um site responsivo e elegante para gerenciar seu programa de fidelidade, cupons e catálogo de produtos.

## 🎯 Funcionalidades

- ✨ Design feminino e moderno
- 📱 Totalmente responsivo (celular, tablet, desktop)
- 🎁 Sistema de pontos e fidelidade
- 🎟️ Gerenciador de cupons personalizados
- 💬 Integração com WhatsApp
- 📸 Integração com Instagram
- 🛍️ Catálogo de produtos

## 📁 Estrutura de Arquivos

```
closet-thayelu/
├── index.html          # Página principal (todo o site em um arquivo)
├── package.json        # Configuração do projeto
├── vercel.json         # Configuração do Vercel
└── README.md           # Este arquivo
```

## 🚀 Como Fazer Deploy no Vercel

### Opção 1: Via GitHub (Recomendado)

1. **Crie um repositório no GitHub:**
   - Vá em [github.com/new](https://github.com/new)
   - Dê o nome: `closet-thayelu`
   - Clique em "Create repository"

2. **Suba os arquivos:**
   - Clique em "uploading an existing file"
   - Arraste os 4 arquivos (`index.html`, `package.json`, `vercel.json`, `README.md`) para o GitHub
   - Clique em "Commit changes"

3. **Conecte ao Vercel:**
   - Vá em [vercel.com](https://vercel.com)
   - Clique em "Add New" > "Project"
   - Selecione o repositório `closet-thayelu`
   - Clique em "Import"
   - Na próxima tela, clique em "Deploy"
   - Aguarde 1-2 minutos e pronto! Seu link estará pronto.

### Opção 2: Deploy Direto (Sem GitHub)

1. Vá em [vercel.com](https://vercel.com)
2. Clique em "Add New" > "Project"
3. Escolha "Clone Template" e procure por "Static Site"
4. Faça upload dos arquivos

## 🎨 Personalizações

### Mudar Cores
Abra o arquivo `index.html` e procure por `#d4a574` (cor principal). Substitua por sua cor preferida.

### Atualizar Contato
Procure por:
- `5583986443504` - Seu número do WhatsApp
- `closetthayelu` - Seu Instagram

### Adicionar Novos Cupons
Procure pela seção "Seus Cupons Exclusivos" e adicione novos cupons no formato:

```html
<div class="coupon-box">
  <div>
    <div class="coupon-code">SEUCUPOM</div>
    <div class="coupon-value">Seu desconto</div>
  </div>
  <button onclick="copiarCupom('SEUCUPOM')" style="background: #d4a574; color: white; border: none; padding: 8px 16px; border-radius: 6px; cursor: pointer; font-size: 12px;">Copiar</button>
</div>
```

### Adicionar Novos Produtos
Procure pela seção "Nossos Produtos" e adicione:

```html
<div class="product-card">
  <div class="product-icon">🧴</div>
  <h3>Nome do Produto</h3>
  <p>Descrição do produto</p>
</div>
```

## 📞 Suporte

Se tiver dúvidas sobre o site, entre em contato:
- WhatsApp: (83) 98644-3504
- Instagram: @closetthayelu

## 📝 Licença

Todos os direitos reservados © 2024 Closet Thay & Lú
