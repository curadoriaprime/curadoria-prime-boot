# 📦 Curadoria Prime — Kit Público de Boot Editorial

Modelos públicos do blog **[Curadoria Prime](https://curadoriaprime.com/)** (reviews e comparativos de tecnologia, Brasil), usados para iniciar sessões de trabalho com agentes de IA já no padrão editorial da casa.

> Tudo aqui é, por natureza, público: o espelho HTML corresponde a um artigo no ar e os padrões E-E-A-T renderizam em todo artigo do site. **Nenhum dado estratégico (pautas, preços capturados, log operacional) vive neste repositório** — isso fica no repositório privado da operação.

## 📁 Arquivos

| Arquivo | O que é |
|---|---|
| `ARTIGO-A-GUTENBERG.html` | **Espelho do modelo Gutenberg da casa** — artigo comparativo publicado (WordPress, blocos `wp:html` com CSS inline, cabeçalho doc-only com campos de SEO, Schema JSON-LD ao final). Referência de estrutura para qualquer artigo novo |
| `CHECKLIST-EEAT-PUBLICO.md` | **Padrões E-E-A-T da casa** — regra-mãe de honestidade, label "Tipo de análise", byline-card do autor, formatos de citação/fontes, regras de QA (versão pública sanitizada do checklist interno) |
| `BLOCO-URLS-PARA-PROMPT.txt` | Bloco pronto para colar na 1ª mensagem de um chat novo — aponta estas URLs raw para o agente ler sozinho |

## ▶️ Como usar num chat novo (Agent Mode)

1. Copie o conteúdo de `BLOCO-URLS-PARA-PROMPT.txt` (ajustando o usuário nas URLs, se necessário).
2. Cole na 1ª mensagem do chat — o agente baixa e lê estes arquivos sem nenhum anexo manual.
3. Contexto sensível que ESTE repo não contém de propósito (handoff de sessão, roadmap de pautas, log-mestre, packs de preço): anexar separadamente, vindos do repositório privado.

## 🧭 Regras públicas da casa (resumo)

- **Honestidade primeiro:** as análises usam pesquisa técnica (fichas oficiais) + testes publicados por canais especializados + dados agregados de compradores verificados. **Nunca** simular teste físico de unidade — o selo "Testado por nós" é reservado para testes reais futuros.
- **Preço sempre com data de verificação** explícita no artigo.
- **Links de afiliado sempre sinalizados** (`rel="sponsored"`) e aviso de comissão no topo dos artigos.
