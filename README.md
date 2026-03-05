README.md# Gestão de Contas Municipais - Itapaci

## Sistema de Controle de Saldos Bancários com Supabase

Site permanente e em tempo real para visualizar os saldos das contas municipais da prefeitura de Itapaci.

### Configuração Atual

- **Supabase Project**: `kgwgovbokrggqyaflobq`
- **Supabase URL**: `https://kgwgovbokrggqyaflobq.supabase.co`
- **Database**: Postgres com 3 tabelas (`accounts`, `banks`, `funds`)
- **Realtime**: Sincroniza a cada 10 segundos

### Como Fazer Deploy no Netlify

#### Opção 1: Conectar via Dashboard Netlify (Recomendado)

1. Vá para: https://app.netlify.com/start
2. Clique em "GitHub"
3. Procure por: `financeiroitapaci-bit/gestor-contas-itapaci`
4. Confirme o deploy
5. Seu site estará pronto em minutos!

#### Opção 2: Usar Netlify CLI

```bash
npm install -g netlify-cli
cd gestor-contas-itapaci
netlify deploy --prod
```

### Como Adicionar Seus Dados

No Supabase SQL Editor, execute:

```sql
INSERT INTO accounts (number, description, area, balance, bank_id, is_active) VALUES
('23203-3', 'FMS – Custeio SUS', 'Saúde', 2356334.07, 1, true),
('573477986-1', 'Emenda Prof. Alcides', 'Executivo', 2021314.39, 1, true),
-- adicione todas as suas 58 contas aqui
;
```

### Arquivos do Projeto

- `index.html` - Página principal com integração Supabase
- `netlify.toml` - Configuração de deploy
- `README.md` - Este arquivo

### Tecnologias

- HTML + CSS + JavaScript vanilla
- Supabase (Postgres + API RESTful)
- Netlify (Hosting)

### Suporte

- Supabase: https://app.supabase.com
- Netlify: https://app.netlify.com
- GitHub: https://github.com
