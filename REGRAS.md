# 📜 Regras do Padrão Editorial — Curadoria Prime

Lista consolidada das regras da casa (fonte: `CHECKLIST-EEAT-PUBLICO.md`), para referência rápida em qualquer sessão de trabalho com agentes de IA.

---

**🛡️ Regra-mãe:** NUNCA simular posse física de produto. O objetivo é provar análise genuína e diferenciada — não fingir unboxing.

---

## 1. Label "Tipo de análise" — OBRIGATÓRIO em todo review

Todo review tem o box:
> **🔍 Tipo de análise:** pesquisa técnica + dados agregados de compradores verificados — não testamos esta unidade fisicamente; quando um artigo tiver teste próprio, ele trará o selo "Testado por nós".

- O selo **✅ "Testado por nós em [data]"** é reservado para testes reais futuros.

## 2. Byline-card da casa

Avatar redondo 72px + nome + credencial + frase honesta + link social (Cristiano Martins, fundador/editor-chefe).

- **Proibido** implicar teste físico na credencial ("testa no uso real de 8h+"). A credencial é *critério de análise*, não laboratório.

## 3. Citações específicas com fonte nomeada

- Trocar estatísticas genéricas por 1–2 avaliações citáveis: **nome semi-anonimizado + data + plataforma**.
- 1 fonte editorial nomeada por artigo, com link na seção Fontes — **confirmar que o link existe antes de citar** (antialucinação).

## 4. Vídeo hands-on — somente com vídeo real confirmado

- Só embutir vídeo cuja existência foi confirmada. Sem vídeo bom → não forçar.

## 5. Síntese "oficial × medido"

- Onde houver teste de terceiro verificável: comparar **spec oficial × medição independente**.
- Sem dado medido verificável → **não inventar**.

## 6. Seção de Fontes — fechar sempre

- Bloco **"📚 Fontes consultadas"**: páginas oficiais do fabricante + 1 análise independente + página(s) de varejo usada(s) nos preços.

## 7. Preço + prova social nas atualizações — OBRIGATÓRIO

1. **Pesquisar preços atuais** no varejo brasileiro (prioritariamente **Amazon** e **Mercado Livre**; + Apple Store/loja oficial quando aplicável).
2. **Pesquisar notas/avaliações de compradores** (estrelas + nº de avaliações).
3. **Atualizar o artigo** com o preço real e data de verificação (`Atualizado: dd/mm/aaaa`) em todos os pontos: hero, cards de "Onde comprar", specs, comparativo e JSON-LD `offers`/`price`.
4. **Renovar a prova social**: bloco "🗣️ O que dizem os compradores" com notas agregadas + citações verificadas + ponto de atenção honesto.
5. **Honestidade**: só usar preços/citações **verificados na fonte** — nunca inventar.

**🕒 Cadência:** reverificar a cada **1–2 meses** por artigo. Se passar do prazo, carregar a ressalva "preços podem estar desatualizados — verifique o valor atual".

## 8. Atualizações sempre no padrão da casa — OBRIGATÓRIO

- Usar estrutura Gutenberg da casa: `wp:heading` (com âncora), `wp:paragraph`, `wp:list`, `wp:html` para componentes.
- **Não** usar HTML cru em bloco único com `<style>` próprio, `<figure>` solto, `<hr class="wp-block-separator">` ou gradientes fora do padrão.
- Manter o fluxo padrão: Tipo de análise → hero → metodologia → índice com âncoras → seções → prova social → "Onde comprar" → veredito → byline → "Fontes consultadas" → JSON-LD.
- Tabelas no estilo da casa (cabeçalho `#1d1d1f` escuro, linhas alternadas), cards verde/vermelho de prós/contrás, veredito em grade de scores.

> **Regra de ouro:** ao atualizar qualquer coisa, garanta que o resultado continua sendo um artigo **no padrão da casa**. Se a origem estava fora do padrão, **reconstrua** para o padrão — não apenas edite o HTML quebrado.

## 9. Prova social — bloco de 4 cards (padrão Apple TV) — OBRIGATÓRIO

- Bloco **"🗣️ O que dizem os compradores"** com **exatamente 4 cards** em grid: 2×2 no desktop, 1 coluna no mobile.
- **2 cards Amazon** (borda/acento laranja `#FF9900`) + **2 cards Mercado Livre** (azul `#3485DB`).
- Cada card: plataforma/variante + `⭐ nota · nº avaliações/opiniões` + 1–2 citações de compra verificada (semi-anonimizada + data + plataforma, conforme regra 3).
- Grid responsiva: `repeat(auto-fit, minmax(240px, 1fr))`.
- **Proibido:** barras de distribuição gigantes, blocos "Aprovado por +N" grandes, logos grandes — nada que ocupe muito espaço e quebre em smartphone.

---

## 🧪 Regras de QA associadas

- Whitelist aos disclaimers negados ("**não** testamos", selo reservado).
- 1ª imagem sem `lazy`, com `fetchpriority="high"`; demais com `loading="lazy"`.
- Meta descrição vive em **2 cópias** (comentário doc-only + bloco `wp:html`) → replace deve bater n=2.
- Medir validações no corpo visível vs arquivo inteiro (comentários doc-only contam).
