# 🛡️ Padrões E-E-A-T — Curadoria Prime (versão pública)

**Base:** diretrizes do Google "Write High Quality Reviews" + boas práticas E-E-A-T.
**Regra-mãe:** NUNCA simular posse física de produto. O objetivo é provar análise genuína e diferenciada — não fingir unboxing.

> ⚠️ Esta é a versão pública sanitizada do checklist interno (ordem de aplicação, metas e log operacional ficam no repositório privado da operação).

---

## 1. Label "Tipo de análise" — OBRIGATÓRIO em todo review

Inserir no box de Metodologia do artigo:

> **🔍 Tipo de análise:** pesquisa técnica + dados agregados de compradores verificados — não testamos esta unidade fisicamente; quando um artigo tiver teste próprio, ele trará o selo "Testado por nós".

- **Selo reservado:** `✅ Testado por nós em [data]` — só para testes reais futuros. A distinção honesta aumenta o valor do selo quando ele existir.

## 2. Byline-card da casa (padrão aprovado em 01/08/2026)

Avatar redondo 72px + nome + credencial + frase honesta + link social. HTML de referência:

```html
<div style="display: flex; gap: 16px; align-items: center; flex-wrap: wrap; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 12px; padding: 18px 20px; margin-bottom: 28px;">
<img src="https://curadoriaprime.com/wp-content/uploads/2026/08/cristian-curadoria-prime.jpg" alt="Cristiano Martins — fundador e editor-chefe da Curadoria Prime" width="72" height="72" style="width: 72px; height: 72px; border-radius: 50%; object-fit: cover; flex-shrink: 0;" loading="lazy">
<div style="font-size: 13.5px; line-height: 1.6; color: #334155; flex: 1; min-width: 240px;">
<strong style="font-size: 14.5px;">Cristiano Martins</strong> — fundador e editor-chefe da Curadoria Prime<br>
<span style="color: #64748b;">Motorista de aplicativo em Uberlândia (MG), com mais de 16 mil viagens entre Uber e 99 e rotina de 8+ horas por dia dependendo de GPS, apps e fones Bluetooth. Fundou a Curadoria Prime para analisar tecnologia por esse critério: o que aguenta o uso real do dia a dia — com preço verdadeiro e ficha técnica oficial.</span><br>
<a href="https://x.com/CuradoriaPrime" rel="noopener" target="_blank" style="color: #1d4ed8; font-weight: 600;">Seguir no X →</a>
</div>
</div>
```

- **Proibido:** "testa tecnologia no uso real de 8h+" (implicaria teste físico que a casa não faz). A credencial é *critério de análise*, não laboratório.

## 3. Citações específicas com fonte nomeada

- Trocar estatísticas genéricas ("+2.000 avaliações") por 1–2 avaliações citáveis: **nome semi-anonimizado + data + plataforma** — ex.: *'"…" — M. R., compra verificada na Amazon, 12/06/2026'*.
- 1 fonte editorial nomeada por artigo (sites especializados BR/gringos), com link na seção Fontes — **confirmar que o link existe antes de citar** (antialucinação).

## 4. Vídeo hands-on embutido — somente com vídeo real confirmado

```html
<!-- wp:html -->
<div style="margin: 0 0 24px; padding: 16px 18px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 12px;">
<p style="margin: 0 0 10px; font-size: 13.5px; font-weight: 700; color: #1e293b;">🎥 Hands-on em vídeo (fonte independente)</p>
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 10px;">
<iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" title="TÍTULO REAL DO VÍDEO" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<p style="margin: 10px 0 0; font-size: 12.5px; color: #64748b; line-height: 1.55;">Teste em vídeo de fonte externa (<a href="https://www.youtube.com/watch?v=VIDEO_ID" rel="noopener" target="_blank">"TÍTULO", YouTube, MÊS/ANO</a>) — referência independente, complementar às especificações oficiais.</p>
</div>
<!-- /wp:html -->
```

⚠️ Só embedar vídeo cuja existência foi confirmada (busca retornando o `/watch?v=`). Sem vídeo bom → não forçar.

## 5. Síntese "oficial × medido"

- Onde houver teste de terceiro verificável: 1–2 linhas comparando **spec oficial × medição independente** (bateria, velocidade, ANC etc.). Formato: *"Oficial × medido (síntese própria): …"*.
- Sem dado medido verificável → **não inventar**.

## 6. Seção de Fontes — fechar sempre

Todo artigo tem o bloco **"📚 Fontes consultadas"** com: páginas oficiais do fabricante + 1 análise independente + página(s) de varejo usada(s) nos preços.

## 7. Preço + prova social nas atualizações — OBRIGATÓRIO

Sempre que um artigo for atualizado (review, comparativo ou guia de compra), o agente/editor deve:

1. **Pesquisar preços atuais** do(s) produto(s) no **varejo brasileiro** — prioritariamente **Amazon** e **Mercado Livre** (pode incluir Apple Store/loja oficial do fabricante quando aplicável).
2. **Pesquisar notas/avaliações de compradores** (classificação em estrelas + nº de avaliações) nas mesmas plataformas.
3. **Atualizar o artigo** com a faixa/preço real capturado e com a **data de verificação** explícita (formato `Atualizado: dd/mm/aaaa`), em todos os pontos onde preço aparece (hero, cards de "Onde comprar", tabela de especificações, comparativo e JSON-LD `offers`/`price`).
4. **Adicionar/renovar a prova social**: bloco **"🗣️ O que dizem os compradores"** com notas agregadas + 1–2 citações de compras verificadas (nome semi-anonimizado + data + plataforma) + ponto de atenção honesto quando houver reclamações recorrentes.
5. **Regra de honestidade**: usar apenas preços e citações **verificados na fonte** — nunca inventar valor, nota ou depoimento. Se não conseguir confirmar, não afirmar.

**Nunca** deixar data/preço desatualizado num artigo sem a ressalva de "verificar valor atual".

**🕒 Cadência de atualização:** reaverificar preços e notas de compradores a cada **1 a 2 meses** por artigo. Se um artigo passar desse intervalo sem atualização de preço/prova social, ele deve carregar a ressalva explícita de "preços podem estar desatualizados — verifique o valor atual" até ser reatualizado.

## 8. Atualizações sempre no padrão da casa — OBRIGATÓRIO

Qualquer atualização de artigo (preço, prova social, correção, reformulação de conteúdo ou layout) **não pode quebrar nem abandonar o padrão da casa**. O espelho HTML versionado e o que vai para o WordPress devem:

- Usar a **estrutura de blocos Gutenberg da casa**: `wp:heading` (com âncora), `wp:paragraph`, `wp:list`, `wp:html` para componentes (cards, tabelas, boxes de aviso) — como no `ARTIGO-A-GUTENBERG.html` e no `Apple-TV-4K.html`.
- **Não** usar HTML cru em bloco único com `<style>` próprio, `<figure>` solto, `<hr class="wp-block-separator">` ou gradientes fora do padrão visual da casa.
- Manter o fluxo padrão: box "Tipo de análise" → hero → metodologia → índice com âncoras → seções com `wp:heading`/âncora → prova social → "Onde comprar" → veredito → byline → "Fontes consultadas" → JSON-LD.
- Preservar as regras 1–7 (label, byline, citações, fontes, preço+prova social) ao atualizar.
- Manter **tabelas no estilo da casa** (cabeçalho `#1d1d1f` escuro, linhas alternadas), cards verde/vermelho de prós/contrás e veredito em grade de scores.

> **Regra de ouro:** ao atualizar qualquer coisa, garanta que o resultado continua sendo um **artigo no padrão da casa**. Se o arquivo de origem estava fora do padrão, a atualização deve **reconstruí-lo** para o padrão — não apenas editar o HTML quebrado.

## 9. Prova social — bloco de 4 cards (padrão Apple TV) — OBRIGATÓRIO

O bloco **"🗣️ O que dizem os compradores"** (prova social) deve seguir o **formato do Apple TV 4K**: **um bloco `wp:html` com exatamente 4 cards** em grid, sendo **2 cards Amazon** (borda/acento laranja `#FF9900`) e **2 cards Mercado Livre** (borda/acento azul `#3485DB`).

**Estrutura e regras:**

- Container: fundo `#f8fafc`, borda `#e2e8f0`, raio 12px, padding 20px 24px, margem inferior 28px.
- Título: `🗣️ O que dizem os compradores` + nota de coleta `(dados coletados em dd/mm/aaaa na Amazon e Mercado Livre)`.
- **Grid responsiva:** `display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px;` — em tela larga forma **2×2 (4 blocos 2 a 2)**; no smartphone empilha em **1 coluna** (cards compactos, sem barras de distribuição ou blocos gigantes).
- Cada card: fundo branco, borda 1px (Amazon `#ffd499` / ML `#a9cdfa`), **border-left 4px** (Amazon `#FF9900` / ML `#3485DB`), raio 10px, padding 14px 16px, fonte 13.5px.
- Conteúdo do card: título da plataforma/variante + `⭐ nota · nº de avaliações/opiniões` + **1–2 citações** de compra verificada (semi-anonimizada + data + plataforma, conforme regra 3).
- Ponto de atenção honesto opcional ao final, quando houver reclamações recorrentes.

**Proibido** no lugar deste bloco: barras de distribuição de estrelas grandes, blocos de "Aprovado por +N" gigantes, logos grandes, ou qualquer layout que ocupe muito espaço vertical e quebre em smartphones.

HTML de referência (modelo a replicar):

```html
<!-- wp:html -->
<div style="background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 12px; padding: 20px 24px; margin-bottom: 28px;">
<p style="margin: 0 0 14px; font-size: 16px; font-weight: 700; color: #1e293b;">🗣️ O que dizem os compradores <span style="font-size: 12px; font-weight: 400; color: #64748b;">(dados coletados em dd/mm/aaaa na Amazon e Mercado Livre)</span></p>
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px;">
<div style="background: #fff; border: 1px solid #ffd499; border-left: 4px solid #FF9900; border-radius: 10px; padding: 14px 16px; font-size: 13.5px;">
<strong style="color: #FF9900;">Amazon — [variante]</strong><br>⭐ <strong>[nota]/5</strong> · <strong>[nº] avaliações</strong><br><em>"[citação]"</em> <span style="color:#64748b;">— compra verificada, [data]</span>
</div>
<div style="background: #fff; border: 1px solid #ffd499; border-left: 4px solid #FF9900; border-radius: 10px; padding: 14px 16px; font-size: 13.5px;">
<strong style="color: #FF9900;">Amazon — destaque</strong><br>⭐ <strong>[nota]/5</strong> · destaque<br><em>"[citação]"</em>
</div>
<div style="background: #fff; border: 1px solid #a9cdfa; border-left: 4px solid #3485DB; border-radius: 10px; padding: 14px 16px; font-size: 13.5px;">
<strong style="color: #3485DB;">Mercado Livre — [variante]</strong><br>⭐ <strong>[nota]/5</strong> · <strong>[nº] opiniões</strong><br><em>"[citação]"</em> <span style="color:#64748b;">— comprador verificado</span>
</div>
<div style="background: #fff; border: 1px solid #a9cdfa; border-left: 4px solid #3485DB; border-radius: 10px; padding: 14px 16px; font-size: 13.5px;">
<strong style="color: #3485DB;">Mercado Livre — destaque</strong><br>⭐ <strong>[nota]/5</strong> · mais vendido<br><em>"[citação]"</em>
</div>
</div>
</div>
<!-- /wp:html -->
```

---

## 🧪 Regras de QA associadas (valem para quem edita os HTMLs)

- Checkers de "claims proibidos" precisam dar **whitelist aos disclaimers negados** ("**não** testamos", selo reservado) — senão o remédio vira falso positivo.
- Ao validar `loading="lazy"`, medir os atributos **depois do `src`** (a primeira imagem do artigo nunca leva lazy; usa `fetchpriority="high"`).
- Textos de meta descrição vivem em **2 cópias** (comentário doc-only + bloco `wp:html`) → qualquer replace deve bater n=2.
- Medir validações no **corpo visível vs arquivo inteiro** (comentários doc-only contam e podem citar histórico de propósito).
