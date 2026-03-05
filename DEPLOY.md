DEPLOY.md# Guia de Deploy - Netlify

## 🚀 DEPLOY RÁPIDO (RECOMENDADO)

### Passo 1: Acesse o Link de Deploy
Clique aqui para fazer o deploy automaticamente:

**https://app.netlify.com/start**

### Passo 2: Conectar GitHub
1. Clique no botão verde **"GitHub"**
2. Procure por: **`financeiroitapaci-bit/gestor-contas-itapaci`**
3. Clique em **"Deploy"`
4. Aguarde 1-2 minutos
5. Pronto! Seu site estará online! 🎉

---

## 💡 ALTERNATIVA: Deploy via CLI (Terminal)

Se preferir usar o terminal (mais rápido):

### Instale o Netlify CLI
```bash
npm install -g netlify-cli
```

### Faça o Deploy
```bash
# 1. Clonar o repositório
git clone https://github.com/financeiroitapaci-bit/gestor-contas-itapaci.git
cd gestor-contas-itapaci

# 2. Fazer login no Netlify
netlify login

# 3. Deploy
netlify deploy --prod
```

Você verá uma URL como: `seu-site.netlify.app`

---

## ✅ Como Funciona

- **Site**: Fica permanentemente online 24/7
- **Dados**: Sincronizam automaticamente a cada 10 segundos com Supabase
- **URL**: Além de `seu-site.netlify.app`, pode usar seu domínio próprio
- **Atualizacao**: Qualquer novo push ao GitHub = novo deploy automático

---

## 🔐 Configuração Supabase (Já Pronta!)

Seu site já está configurado para conectar ao Supabase:

- **URL**: https://kgwgovbokrggqyaflobq.supabase.co
- **Chave**: sb_publishable_xeS3d_NFqLVm-IPLpXnlCA_Fi7cC_Hz
- **Tabelas**: accounts, banks, funds

O arquivo `index.html` já possui todo o código necessário!

---

## 📝 Próximos Passos

1. **Fazer Deploy** (acima)
2. **Adicionar Suas Contas** no Supabase
3. **Ver os Dados em Tempo Real** no seu site
4. **Compartilhar o Link** com quem precisar

Qualém tiver o link poderá ver os dados atualizados automaticamente a cada 10 segundos!

---

## 📄 Adicionar Seus Dados (58 Contas)

No **Supabase SQL Editor**:

```sql
INSERT INTO accounts (number, description, area, balance, bank_id, is_active) VALUES
('23203-3', 'FMS – Custeio SUS', 'Saúde', 2356334.07, 1, true),
('573477986-1', 'Emenda Prof. Alcides', 'Executivo', 2021314.39, 1, true),
-- adicione todas as suas 58 contas aqui
;
```

Depois que adicionar, o site já mostrará os dados!

---

## 🏘 Suporte

- Dificuldade com GitHub? Veja: https://docs.github.com/pt
- Dúvida no Netlify? Veja: https://docs.netlify.com/
- Supabase: https://app.supabase.com

**Tudo pronto! Basta clicar em Deploy!** 🙋
