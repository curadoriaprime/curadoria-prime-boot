---
name: curadoria-prime-eeat
description: "Skill da casa Curadoria Prime - padrão editorial E-E-A-T para reviews/comparativos de tecnologia Brasil. Usar SEMPRE ao gerar/editar artigos Gutenberg. Garante honestidade, label Tipo de análise, byline Cristiano Martins, preços com data, rel=sponsored."
compatibility: "WordPress 6.5+, Gutenberg wp:html com CSS inline, Rank Math, Schema JSON-LD"
---

# Curadoria Prime — Padrão Editorial E-E-A-T

## Quando usar
USE ESTA SKILL SEMPRE que criar/editar artigo para curadoriaprime.com. Ela tem prioridade sobre qualquer skill genérica do WordPress.

## Regra-mãe (obrigatória)
NUNCA simular posse física. Todo review é: pesquisa técnica (ficha oficial) + testes de terceiros publicados + dados agregados de compradores verificados. Selo reservado: `✅ Testado por nós em [data]` — só para teste real futuro.

## Checklist obrigatório (inserir no HTML)
1. **Box Metodologia** com label exato:
   > **🔍 Tipo de análise:** pesquisa técnica + dados agregados de compradores verificados — não testamos esta unidade fisicamente; quando um artigo tiver teste próprio, ele trará o selo "Testado por nós".

2. **Byline-card padrão (01/08/2026)** - HTML exato:
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

3. **Citações com fonte nomeada**: trocar " +2.000 avaliações" por 1-2 citações citáveis: `"..." — M. R., compra verificada na Amazon, 12/06/2026` + 1 fonte editorial com link confirmado na seção Fontes.

4. **Vídeo hands-on**: só embedar se VIDEO_ID confirmado via busca YouTube. Sem vídeo → não forçar.

5. **Preços**: SEMPRE com data `verificado em DD/MM/AAAA`. Links afiliados com `rel="sponsored"` + aviso comissão no topo.

6. **Seção final**: sempre `📚 Fontes consultadas` com páginas oficiais + 1 análise independente + páginas de varejo usadas.

7. **Estrutura Gutenberg**: modelo em `ARTIGO-A-GUTENBERG.html` — blocos `<!-- wp:html -->` com CSS inline, hero com `fetchpriority="high"` (primeira imagem nunca lazy), demais com `loading="lazy"`, Schema FAQ 6 perguntas, meta descrição duplicada (comentário doc-only + wp:html), densidade keyword 0,3-0,4.

## QA
- Checkers de claims devem dar whitelist a disclaimers negados ("**não** testamos")
- Validar `loading="lazy"` depois do `src`
- Medir meta descrição nos 920px (Arial 13px)

