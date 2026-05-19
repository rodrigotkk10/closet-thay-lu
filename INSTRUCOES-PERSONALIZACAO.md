# 📖 Instruções de Personalização - Closet Thay & Lú

## 🎯 Visão Geral das Melhorias

Seu site foi completamente atualizado com as seguintes funcionalidades:

1. **Vitrine de Produtos com Fotos** - Seção visual com imagens dos produtos
2. **Sistema de Fidelidade Aprimorado** - Pontos por compra + pontos por indicação
3. **Simulador de Cupom** - Crie cupons personalizados em tempo real
4. **Responsividade Total** - Perfeito para WhatsApp e celulares

---

## 🛍️ Como Adicionar/Editar Produtos

### Passo 1: Abra o arquivo `index-melhorado.html`

### Passo 2: Procure pela seção "CONFIGURAÇÃO DE PRODUTOS" (linha ~340)

Você encontrará algo assim:

```javascript
const products = [
  {
    id: 1,
    name: "Shampoo Premium",
    description: "Limpeza profunda e brilho intenso",
    price: "R$ 45,00",
    image: "https://via.placeholder.com/300x300?text=Shampoo+Premium",
    emoji: "🧴"
  },
  {
    id: 2,
    name: "Condicionador Luxo",
    description: "Hidratação e maciez garantidas",
    price: "R$ 50,00",
    image: "https://via.placeholder.com/300x300?text=Condicionador",
    emoji: "💆"
  },
  // ... mais produtos
];
```

### Passo 3: Edite os Campos

Para cada produto, você pode editar:

| Campo | O que fazer | Exemplo |
|-------|-----------|---------|
| **id** | Número único (1, 2, 3...) | `1` |
| **name** | Nome do produto | `"Shampoo Premium"` |
| **description** | Descrição curta | `"Limpeza profunda e brilho intenso"` |
| **price** | Preço com símbolo R$ | `"R$ 45,00"` |
| **image** | URL da foto (veja abaixo) | `"https://..."` |
| **emoji** | Emoji de fallback | `"🧴"` |

### Passo 4: Adicione suas Fotos

Você tem 3 opções:

#### Opção A: Usar URL de Foto Hospedada (Recomendado)
Se você tem as fotos em um servidor ou Google Drive:

```javascript
image: "https://drive.google.com/uc?export=view&id=SEU_ID_AQUI"
```

#### Opção B: Usar Imgur ou Similar
1. Acesse [imgur.com](https://imgur.com)
2. Faça upload da foto
3. Copie o link da imagem
4. Cole no campo `image`

#### Opção C: Usar Placeholder (Temporário)
Enquanto não tem as fotos reais:

```javascript
image: "https://via.placeholder.com/300x300?text=Nome+do+Produto"
```

### Passo 5: Adicione Novos Produtos

Para adicionar um novo produto, copie um bloco inteiro e adicione uma vírgula:

```javascript
const products = [
  {
    id: 1,
    name: "Shampoo Premium",
    description: "Limpeza profunda e brilho intenso",
    price: "R$ 45,00",
    image: "https://...",
    emoji: "🧴"
  },
  {
    id: 2,
    name: "Seu Novo Produto",
    description: "Descrição do novo produto",
    price: "R$ XX,XX",
    image: "https://...",
    emoji: "🎁"
  }  // ← Não esqueça da vírgula!
];
```

---

## 🎟️ Como Criar Cupons Personalizados

### Método 1: Usar o Simulador (Na Página)

1. Acesse a página no navegador
2. Vá até a seção "Seus Cupons Exclusivos"
3. Preencha os campos:
   - **Nome do cupom**: ex: `MARIA10`
   - **Tipo**: escolha entre `% Desconto`, `R$ Desconto` ou `Brinde`
   - **Valor**: ex: `10` (para 10% ou R$ 10)
4. Veja o preview ao vivo
5. Compartilhe com o cliente

### Método 2: Editar Diretamente no Código (Para Cupons Fixos)

Procure pela seção de cupons (linha ~450) e adicione novos:

```html
<div class="coupon-box">
  <div>
    <div class="coupon-code">SEUCUPOM20</div>
    <div class="coupon-value">20% de desconto</div>
  </div>
  <button onclick="copiarCupom('SEUCUPOM20')" style="background: #d4a574; color: white; border: none; padding: 8px 16px; border-radius: 6px; cursor: pointer; font-size: 12px;">Copiar</button>
</div>
```

---

## 💳 Sistema de Fidelidade - Como Funciona

### Pontos por Compra
- Cliente compra → ganha **1 ponto**
- Acumula **5 pontos** → ganha um **brinde exclusivo**

### Pontos por Indicação
- Cliente indica uma amiga → ganha **1 ponto**
- Amiga indicada faz sua 1ª compra → ganha **1 ponto** também
- Ambas ganham pontos!

### Exemplo:
```
Maria compra → Maria ganha 1 ponto
Maria indica Joana
Joana faz sua 1ª compra → Maria ganha 1 ponto (indicação) + Joana ganha 1 ponto (compra)
Maria agora tem 3 pontos no total!
```

---

## 🔧 Personalizações Adicionais

### Mudar Número do WhatsApp

Procure por `5583986443504` no arquivo e substitua pelo seu número:

```html
<!-- Antes -->
<a href="https://wa.me/5583986443504?text=...">

<!-- Depois -->
<a href="https://wa.me/SEUNUMERO?text=...">
```

**Formato do número**: `55` (Brasil) + `83` (DDD) + `98644-3504` (número)
**Sem símbolos**: `5583986443504`

### Mudar Instagram

Procure por `closetthayelu` e substitua:

```html
<!-- Antes -->
<a href="https://instagram.com/closetthayelu">

<!-- Depois -->
<a href="https://instagram.com/SEUUSUARIO">
```

### Mudar Cores Principais

A cor principal é `#d4a574` (bege/ouro). Para mudar:

1. Abra o arquivo em um editor de texto
2. Use Ctrl+H (ou Cmd+H) para "Localizar e Substituir"
3. Procure por: `#d4a574`
4. Substitua por: sua cor em hexadecimal (ex: `#FF6B9D`)

**Cores sugeridas**:
- Rosa: `#FF6B9D`
- Roxo: `#9B59B6`
- Azul: `#3498DB`
- Verde: `#27AE60`

---

## 📱 Testando a Responsividade

### No Navegador:
1. Abra o arquivo no Chrome/Firefox
2. Pressione `F12` (ou Cmd+Option+I no Mac)
3. Clique no ícone de celular (ou Ctrl+Shift+M)
4. Teste em diferentes tamanhos

### No Celular:
1. Salve o arquivo
2. Envie para você mesmo via WhatsApp
3. Abra no celular e teste os botões

---

## 🚀 Deploy no GitHub/Vercel

### Passo 1: Renomear o arquivo

```bash
# Renomeie index-melhorado.html para index.html
mv index-melhorado.html index.html
```

### Passo 2: Fazer commit e push

```bash
git add index.html
git commit -m "Atualizar vitrine de produtos e sistema de fidelidade"
git push origin main
```

### Passo 3: Vercel atualiza automaticamente

Seu site estará atualizado em segundos!

---

## ⚠️ Cuidados Importantes

### ✅ SEGURO fazer:
- Editar nomes, descrições e preços dos produtos
- Adicionar novos produtos
- Mudar cores e emojis
- Atualizar cupons
- Trocar links de WhatsApp/Instagram

### ❌ NÃO fazer:
- Deletar tags HTML inteiras (como `<div>`, `<button>`, etc.)
- Mudar nomes de funções JavaScript (como `toggleFaq`, `copiarCupom`)
- Remover a seção `<script>` do final
- Adicionar espaços em branco desnecessários dentro de tags

---

## 🐛 Se Algo Quebrar

### Problema: Página não carrega
**Solução**: Verifique se não há erros de digitação. Procure por:
- Aspas faltando (`"` ou `'`)
- Vírgulas faltando (`,`)
- Chaves faltando (`{`, `}`)

### Problema: Botão não funciona
**Solução**: Verifique se o link do WhatsApp está correto:
```
https://wa.me/SEUNUMERO?text=...
```

### Problema: Produtos não aparecem
**Solução**: Verifique se a lista `const products = [...]` está correta e sem erros de sintaxe.

---

## 📞 Suporte

Se tiver dúvidas sobre como usar o site, entre em contato com a equipe de desenvolvimento. 

Para edições futuras, lembre-se:
1. Sempre fazer backup do arquivo antes de editar
2. Testar as mudanças localmente antes de fazer push
3. Usar um editor de texto com destaque de sintaxe (VS Code, Sublime Text, etc.)

---

## 📋 Checklist de Implementação

- [ ] Adicionar suas fotos dos produtos
- [ ] Atualizar preços
- [ ] Testar botão "Eu quero esse!" no WhatsApp
- [ ] Criar cupons personalizados
- [ ] Testar responsividade no celular
- [ ] Fazer commit e push para GitHub
- [ ] Verificar se atualizou no Vercel
- [ ] Compartilhar link com clientes!

---

**Pronto para começar? Boa sorte! 🎉**
