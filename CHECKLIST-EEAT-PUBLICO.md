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

---

## 🧪 Regras de QA associadas (valem para quem edita os HTMLs)

- Checkers de "claims proibidos" precisam dar **whitelist aos disclaimers negados** ("**não** testamos", selo reservado) — senão o remédio vira falso positivo.
- Ao validar `loading="lazy"`, medir os atributos **depois do `src`** (a primeira imagem do artigo nunca leva lazy; usa `fetchpriority="high"`).
- Textos de meta descrição vivem em **2 cópias** (comentário doc-only + bloco `wp:html`) → qualquer replace deve bater n=2.
- Medir validações no **corpo visível vs arquivo inteiro** (comentários doc-only contam e podem citar histórico de propósito).
