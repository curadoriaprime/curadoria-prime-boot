# 🔎 Análise do artigo — "Edifier W820NB Review 2026: O Melhor Headphone ANC Over-Ear Até R$400?"

**Espelho analisado:** `artigos-publicados/edifier-w820nb-review-2026.html` (branch `arena/019feb2f-...`, 631 linhas)
**Nota do artigo (no corpo):** 8,8/10
**Data declarada:** Março de 2026
**Base de análise:** HTML versionado + `CHECKLIST-EEAT-PUBLICO.md` (regra-mãe, labels, byline, QA) + README

---

## ⚠️ Prioridade 1 — CONTRADIÇÃO CRÍTICA E-E-A-T: teste físico inventado vs metodologia

**Este é o problema mais grave de todos os artigos que analisei.** A casa tem uma regra-mãe absoluta:

> **"NUNCA simular posse física de produto"** + o selo `✅ Testado por nós` é **reservado** para testes reais futuros.

O artigo **se contradiz internamente**:

- **Box de metodologia (topo, linha 18):** `não testamos esta unidade fisicamente` — correto per a regra.
- **Corpo do artigo (repetidamente afirma teste físico próprio):**
  - *"Este Edifier W820NB review foi feito por quem usou o headphone por mais de duas semanas em home office..."* (linha 42)
  - H2 5: *"...ANC de 38dB: O Mais Forte da Lista — **Testamos**"* (título)
  - *"Na prática, **testamos em três cenários** de uso"* (modo gamer)
  - *"**Testamos em chamadas reais** no Google Meet, Microsoft Teams e WhatsApp durante a semana de avaliação"*
  - *"**Testamos as duas situações** ao longo de uma semana"* (bateria)
  - Seções de conforto com relatos de "Sessão de 2h/4h/6h" e "Autonomia real medida" em tabela
- **Aviso de atualização (rodapé, linha 587):** *"Produto analisado: Edifier W820NB Cinza (**unidade adquirida pelo autor**)"* — afirma posse física.

Ou seja: o texto diz "não testamos" no box, mas o corpo inteiro é escrito como um hands-on real com posse da unidade. Isso é exatamente o que a regra-mãe proíbe — e um risco E-E-A-T/Google alto.

### 🟢 Se o produto FOI realmente testado (só o editor sabe)
Aí a correção é **no box de metodologia e no label**, não no corpo:
- Trocar "não testamos esta unidade fisicamente" → **`✅ Testado por nós em [data]`**
- Ajustar o box "Tipo de análise" e o byline para refletir teste real.

### 🔴 Se o teste foi inventado/editado como hands-on simulado (regra da casa)
Aí a correção é **no corpo do artigo**: reescrever/neutralizar todas as afirmações de teste físico e posse, atribuindo os achados a: especificações oficiais + avaliações de compradores verificados + testes de canais especializados (como o checklist manda), e manter o box "não testamos".

---

## Prioridade 2 — Problemas técnicos / HTML

| # | Problema | Detalhe |
|---|---|---|
| 1 | **`<br />` dentro do `<style>`** | 8 ocorrências de `<br />` no meio do CSS (ex.: `... color:#333; line-height:1.7; padding:20px; }<br />`). HTML inválido — quebra o parsing do bloco de estilo e pode vazar texto. |
| 2 | **`<figure>` vazio** | Linha 87: `<figure style="text-align: center; margin: 20px 0;"></figure>` — figura sem imagem, só cria espaço vazio na seção 2. |
| 3 | **JSON-LD muito enxuto** | Só um `TechArticle` com headline/description/author. **Sem** `reviewRating` (o 8,8/10 não está no schema), sem `offers`, sem `FAQPage` (apesar de ter FAQ grande), sem imagem, sem `datePublished/dateModified`. Comparado ao da Apple TV, está incompleto e perde rich-snippets. |
| 4 | **Meta description ausente** | Não há o comentário doc-only `META DESCRIÇÃO SEO` (presente na Apple TV). O `description` do JSON-LD é genérico: *"Edifier W820NB Review 2026: Vale a Pena? Veja o veredito."* — não descreve preço/ANC nem intenção. |
| 5 | **Consistência da imagem do byline** | Usa `cristian-curadoria-prime.jpg`, enquanto a Apple TV usa `cristiano-curadoria-prime.jpg`. Confirmar qual existe no media library (uma das duas quebra). |

## Prioridade 3 — Conformidade E-E-A-T (o que está OK)

- ✅ Label "🔍 Tipo de análise" + "não testamos" no box de metodologia (mesmo que o corpo contradiga — ver P1).
- ✅ Aviso de transparência/afiliado no topo.
- ✅ Links de afiliado com `rel="sponsored nofollow noopener"` (4 ocorrências).
- ✅ Byline-card padrão no rodapé (nome, credencial, link social) — exceto nome do arquivo da imagem (P2.5).
- ✅ Autor no JSON-LD já está como "Cristiano Martins" (consistente).
- ✅ 1ª imagem com `fetchpriority="high"` sem lazy.
- ✅ "Veja também" e links internos do cluster presentes.
- ✅ Transparência honesta em vários pontos (ex.: "não é o Sony XM5", "calor das almofadas").

## Prioridade 4 — Conteúdo / consistência factual

- **Datas ambíguas:** "março de 2026" repetido em vários pontos; a tabela comparativa diz "Preço (março 2026)" e o rodapé "Última atualização: Março de 2026". Sem data-dia, mas consistente. OK, porém sem o padrão "Atualizado em [dd/mm/aaaa]" do topo.
- **Duplicidade de preço:** header diz "R$ 399", specs "~R$ 399 | 5% OFF no Pix = R$ 379", card de compra "~R$ 399". Coerente, mas vale unificar o "melhor preço de hoje" com data.
- **Número de micro...** — "dois microfones" no corpo vs app/features; ok.
- **Posição em rankings:** o texto diz "único over-ear" e "melhor headphone ANC até R$400" — afirmações de ranking que dependem do guia-âncora (link interno). Coerente.

---

## Diagnóstico geral

**Nota de conformidade E-E-A-T: baixa por causa da P1** — o artigo é bem escrito, útil e honesto em vários pontos, mas a **simulação de teste físico/posse contradiz a regra-mãe da casa** e é um risco real. Isso precisa ser resolvido antes de qualquer coisa (P1). Os problemas técnicos (P2) são objetivos e fáceis de corrigir.

---

## Layout — reconstruído no padrão da casa (Gutenberg)

O espelho original **não seguia o padrão da casa**: era um único bloco cru com `<style>` próprio, gradientes roxos, `<figure>`, `<hr class="wp-block-separator">` e quase nenhum bloco Gutenberg (só 8 `wp:html`, sem `wp:heading`/`wp:paragraph`/`wp:list`).

**Reconstruí no padrão da casa** (mesma estrutura do Apple TV / `ARTIGO-A-GUTENBERG`):
- Box de "Tipo de análise" + hero escuro com selos + imagem destacada + metodologia + índice com âncoras.
- Cada seção como `wp:heading` (com âncora) + `wp:paragraph` + `wp:html` (tabelas/cards).
- Tabelas no estilo da casa (cabeçalho `#1d1d1f`, linhas alternadas).
- Prós/Contras e "para quem é/não é" em cards verde/vermelho; veredito em grade de scores.
- FAQ, especificações, onde comprar, veja também, byline, fontes e JSON-LD fechando.
- **Validação:** 37 `wp:html`, 21 `wp:paragraph`, 19 `wp:heading` (todos balanceados), 17 âncoras do índice com IDs correspondentes, JSON-LD com 4 nós válido. Zero resquício do formato antigo (`<style>`, `wp-block-group`, `<figure>`, `<hr>`).

---

## Plano de correção — APLICADO (conforme metodologia do site)

> Decisão do editor: **corrigir conforme a metodologia do site** (pesquisa técnica + canais especializados + dados de compradores; nunca simular teste físico). Complementei com pesquisas oficiais (Edifier BR) e de canais (Tecnoblog, Canaltech, Prime Audio Reviews).

**✅ Corrigido neste ciclo (arquivo `artigos-publicados/edifier-w820nb-review-2026.html` na branch):**
- [x] **P1:** neutralizei todas as afirmações de teste físico/posse (intro "usou por duas semanas", título "— Testamos", "Testamos em três cenários", "Testamos em chamadas reais", "Testamos as duas situações", tabela "Autonomia real medida", rodapé "unidade adquirida pelo autor") — agora atribuídos a ficha oficial + canais especializados + relatos de compradores, mantendo o box "não testamos esta unidade fisicamente".
- [x] **P2.1:** removidos os 8 `<br />` de dentro do `<style>`.
- [x] **P2.2:** removido o `<figure>` vazio.
- [x] **P2.3:** JSON-LD enriquecido — agora tem `Article` + `Review` (rating 8.8/10, offers R$399) + `FAQPage` (4 perguntas) + `BreadcrumbList` (4 nós no `@graph`, validado).
- [x] **P2.4:** adicionada meta description real (doc-only + `description` do schema).
- [x] **P2.5:** verificado — o byline usa `cristian-curadoria-prime.jpg`, que é o padrão do checklist da casa (correto).

**➕ Extra (factual, de pesquisa):** a seção 9 afirmava "Equalizador de 10 bandas" no app, mas o Tecnoblog e a página oficial da Edifier indicam que o app do W820NB **não tem equalizador**. Corrigi a lista de recursos (ANC ajustável, modo ambiente, modo gamer, bateria, firmware) e reescrevi o fechamento honestamente.
