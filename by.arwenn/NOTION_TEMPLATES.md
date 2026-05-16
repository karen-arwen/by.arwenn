# 🗂 TEMPLATES DE NOTION — SISTEMA DE GESTÃO ARWEN

> Estruturas prontas pra montar seu "cérebro central" no Notion. Cria uma página chamada "ARWEN HQ" e dentro dela essas 6 databases.  
> Notion é grátis pra uso pessoal. Baixa no notion.so. Cada seção abaixo = uma database (tabela) que você recria no Notion.

---

## 🏠 ESTRUTURA GERAL — "ARWEN HQ"

```
📁 ARWEN HQ
├── 📊 1. CRM de Marcas (database)
├── 💡 2. Banco de Ideias (database)
├── 📅 3. Calendário de Conteúdo (database)
├── 🤝 4. Parcerias & Contratos (database)
├── 📈 5. Métricas Semanais (database)
└── ✅ 6. Metas & Hábitos (database)
```

Cada uma é uma "Tabela" no Notion (botão `/database` ou `/table`).

---

## 📊 DATABASE 1 — CRM DE MARCAS

**Pra que serve:** controlar toda prospecção. Quem você contatou, status, próximo passo.

### Propriedades (colunas):

| Coluna | Tipo no Notion | Opções |
|---|---|---|
| Marca | Title (texto) | — |
| Categoria | Select | Games, Beleza, Livros, Tech, Colecionáveis, Evento, Plataforma, Agência |
| Temperatura | Select | 🔥 Quente, ⭐ Morna, 💫 Aspiracional |
| Canal de contato | Text | e-mail / DM / formulário |
| Data do 1º contato | Date | — |
| Status | Select | A fazer, Enviado, Follow-up, Respondeu, Em negociação, Fechado, Recusado, Arquivado |
| Resposta | Text | resumo do que responderam |
| Próximo passo | Text | o que fazer agora |
| Data próximo passo | Date | — |
| Valor proposto | Number | R$ |
| Notas | Text | observações |

### Views (visualizações) recomendadas:
- **"A fazer"** → filtro: Status = A fazer (ordenado por Temperatura)
- **"Aguardando follow-up"** → filtro: Status = Enviado E Data 1º contato > 7 dias atrás
- **"Em negociação"** → filtro: Status = Em negociação
- **"Fechadas"** → filtro: Status = Fechado

### Conteúdo inicial pra preencher:
Copia da `LISTA_MARCAS_PROSPECCAO.md` — os 10 alvos prioritários já entram aqui como "A fazer".

---

## 💡 DATABASE 2 — BANCO DE IDEIAS

**Pra que serve:** nunca mais "não sei o que postar". Toda ideia que surgir, joga aqui.

### Propriedades:

| Coluna | Tipo | Opções |
|---|---|---|
| Ideia | Title | descrição curta |
| Nicho | Select | Games, Nintendo, Livros, Manhwa, Make, Anime, Opinião, Colecionável, Lifestyle, Crossover |
| Quadro | Select | Arwen Reage, A Arwen Indica, Arwen se Arruma, Arwen Joga, Surto Geek, Arwen Testa, Arwen no Evento, Arwen Tem Opinião |
| Formato | Select | Reel, Carrossel, Stories, Vídeo longo, UGC |
| Status | Select | 💭 Ideia, ✍️ Roteiro, 🎬 Gravado, ✂️ Editado, ✅ Postado |
| Prioridade | Select | Alta, Média, Baixa |
| Trend? | Checkbox | marca se é baseado em trend (tem prazo) |
| Roteiro | Text / Page | link ou texto do roteiro |
| Data ideal | Date | quando faz sentido postar |

### Views:
- **"Próximas a gravar"** → filtro: Status = Roteiro, ordenado por Prioridade
- **"Por nicho"** → agrupado por Nicho
- **"Trends urgentes"** → filtro: Trend = ✓ E Status ≠ Postado
- **"Pipeline"** → board view agrupado por Status (estilo Kanban)

### Conteúdo inicial:
- Os 10 roteiros do `BACKLOG_10_VIDEOS.md` entram aqui como "Roteiro" pronto
- As 5 ideias do `TRENDS_2026_ADAPTADAS.md` entram como "Ideia"
- Seu banco de 150+ ideias que já existe → migra pra cá aos poucos

---

## 📅 DATABASE 3 — CALENDÁRIO DE CONTEÚDO

**Pra que serve:** ver o mês inteiro, planejar com antecedência, não furar postagem.

### Propriedades:

| Coluna | Tipo | Opções |
|---|---|---|
| Post | Title | nome do conteúdo |
| Data | Date | data + hora de publicação |
| Plataforma | Multi-select | Instagram, TikTok, YouTube |
| Formato | Select | Reel, Carrossel, Stories, Short, Vídeo |
| Nicho | Select | (mesmos do Banco de Ideias) |
| Status | Select | 📋 Planejado, 🎬 Produzindo, ⏰ Agendado, ✅ Publicado |
| Legenda | Text | caption pronta |
| Hashtags | Text | conjunto de hashtags |
| Link da ideia | Relation | conecta com Database 2 |

### Views:
- **"Calendário"** → Calendar view (vê o mês todo)
- **"Essa semana"** → filtro: Data nessa semana
- **"A produzir"** → filtro: Status = Planejado ou Produzindo

### Conteúdo inicial:
Copia o `CALENDARIO_30_DIAS.md` inteiro pra cá — 30 dias já mapeados.

---

## 🤝 DATABASE 4 — PARCERIAS & CONTRATOS

**Pra que serve:** controlar parcerias fechadas — entregas, prazos, pagamentos, NF.

### Propriedades:

| Coluna | Tipo | Opções |
|---|---|---|
| Parceria | Title | Marca + campanha |
| Marca | Relation | conecta com CRM (Database 1) |
| Tipo | Select | UGC, Post patrocinado, Review, Evento, Long-term, Permuta |
| Valor | Number | R$ |
| Status | Select | Negociando, Contrato enviado, Assinado, Produzindo, Entregue, Pago, Encerrado |
| Briefing recebido? | Checkbox | — |
| Contrato assinado? | Checkbox | — |
| Data entrega | Date | prazo combinado |
| Data publicação | Date | quando vai ao ar |
| 50% antecipado pago? | Checkbox | — |
| Pagamento final | Checkbox | — |
| NF emitida? | Checkbox | — |
| Link do conteúdo | URL | post final |
| Notas | Text | — |

### Views:
- **"Ativas"** → filtro: Status ≠ Encerrado
- **"Aguardando pagamento"** → filtro: Entregue = ✓ E Pagamento final = ✗
- **"Pra emitir NF"** → filtro: Pago = ✓ E NF = ✗
- **"Histórico"** → todas, ordenado por data

### Por que isso importa:
No fim do ano, essa database É sua declaração de IR. E cada linha vira um CASE pro portfólio.

---

## 📈 DATABASE 5 — MÉTRICAS SEMANAIS

**Pra que serve:** acompanhar crescimento, ver o que funciona, ajustar estratégia.

### Propriedades:

| Coluna | Tipo | Opções |
|---|---|---|
| Semana | Title | "Semana 13-19/05" |
| Data fechamento | Date | segunda-feira da medição |
| Seguidores IG | Number | total |
| Ganho de seguidores | Number | da semana |
| Views totais | Number | da semana |
| Engajamento médio | Number | (likes+coments+saves)/posts |
| Shares totais | Number | a métrica-chave de 2026 |
| Seguidores TikTok | Number | — |
| Inscritos YouTube | Number | — |
| E-mails enviados | Number | — |
| Respostas de marca | Number | — |
| Receita da semana | Number | R$ |
| Melhor post | Text | qual foi e por quê |
| Aprendizado | Text | o que ajustar |

### Views:
- **"Tabela"** → todas as semanas (vê a evolução linha a linha)
- **"Gráfico"** → adiciona um gráfico de linha pra Seguidores IG ao longo do tempo

### Rotina:
Toda segunda 8h, 5 minutos preenchendo. No fim do trimestre, você VÊ o crescimento.

---

## ✅ DATABASE 6 — METAS & HÁBITOS

**Pra que serve:** acompanhar as metas do `ESTRATEGIA_CRESCIMENTO.md` e os hábitos diários.

### Parte A — Metas (database simples):

| Coluna | Tipo | Opções |
|---|---|---|
| Meta | Title | — |
| Prazo | Date | — |
| Categoria | Select | Crescimento, Receita, Conteúdo, Prospecção, Plataforma |
| Status | Select | Não iniciada, Em progresso, Concluída |
| Progresso | Number | % ou número atual |
| Meta numérica | Number | alvo |

Conteúdo inicial: copia as metas do `ESTRATEGIA_CRESCIMENTO.md` (5k seguidores, 6 parcerias, etc.).

### Parte B — Hábitos diários (checkbox tracker):
Lista simples de hábitos pra marcar todo dia:
- [ ] Respondi todos os comentários (2h após postar)
- [ ] Engajei em 5 contas do nicho
- [ ] 10 min de pesquisa de trend
- [ ] Stories postados (2-5)
- [ ] Atualizei o CRM/calendário

---

## 🎨 DICA DE ESTÉTICA NO NOTION

Pra ficar a cara da Arwen:
- **Cover das páginas:** imagem lilás (Unsplash busca "purple aesthetic")
- **Ícones:** emojis consistentes (✦ 💜 🎮 📚)
- **Cor de destaque:** roxo nos selects sempre que possível
- **Página inicial "ARWEN HQ":** adiciona uma frase do manifesto no topo (do POSICIONAMENTO_MARCA.md)

---

## 🚀 COMO MONTAR (passo a passo)

1. Cria conta grátis em **notion.so** (usa o e-mail de parcerias)
2. Cria uma página: **"ARWEN HQ"**
3. Dentro dela, cria 6 sub-páginas (uma por database acima)
4. Em cada sub-página, digita `/table` e cria a tabela
5. Adiciona as colunas conforme as tabelas acima
6. Cria as Views recomendadas
7. Preenche o conteúdo inicial (vem dos outros arquivos do projeto)
8. Fixa a página "ARWEN HQ" nos favoritos do Notion

**Tempo de montagem:** ~2 horas numa tarde. Depois é só manter.

---

## 🔁 ALTERNATIVA RÁPIDA — GOOGLE SHEETS

Se Notion parecer complexo demais agora, faz a versão simplificada no Google Sheets:
- 1 aba "CRM Marcas"
- 1 aba "Calendário"
- 1 aba "Parcerias"
- 1 aba "Métricas"

Mesmas colunas, menos bonito, mas funciona. Migra pro Notion quando tiver fôlego.

---

## 📌 ROTINA DE USO DO SISTEMA

| Quando | O que fazer |
|---|---|
| **Toda manhã (5 min)** | Olha "A fazer" no CRM + "Próximas a gravar" no Banco de Ideias |
| **Toda segunda (15 min)** | Preenche Métricas Semanais + revisa Metas |
| **Toda quinta (20 min)** | Envia e-mails de prospecção + atualiza CRM |
| **Todo domingo (30 min)** | Planeja semana no Calendário + agenda posts |
| **Quando fecha parceria** | Cria linha em Parcerias & Contratos |
| **Quando tem ideia** | Joga no Banco de Ideias na hora (nem que seja 1 linha) |

---

💜 **Quer que eu monte uma versão em Google Sheets pronta pra você importar?** Posso gerar o arquivo .xlsx com todas as abas e colunas já estruturadas. Me avisa.
