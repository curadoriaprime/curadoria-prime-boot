# 🚚 Guia de portabilidade — levando o agente Curadoria Prime para outros ambientes

Este kit foi desenhado para **Agent Mode** (o agente faz fetch das URLs raw sozinho via `BLOCO-URLS-PARA-PROMPT.txt`). Em outros ambientes o mecanismo de entrega muda — o agente em si (arquivos + regras) é o mesmo.

> 📦 **Esta pasta é 100% separada do kit original.** Os 4 arquivos da raiz (`README.md`, `ARTIGO-A-GUTENBERG.html`, `CHECKLIST-EEAT-PUBLICO.md`, `BLOCO-URLS-PARA-PROMPT.txt`) seguem intocados — nada daqui precisa estar na raiz, e a pasta pode ser removida sem afetar o boot do Agent Mode.

## 📁 O que há nesta pasta

| Arquivo | Uso |
|---|---|
| `GUIA-PORTABILIDADE.md` | Este guia |
| `BLOCO-CLAUDE-AI.txt` | 1ª mensagem para o Claude.ai (arquivos anexados, sem fetch de URL) |
| `BLOCO-VSCODE.txt` | 1ª mensagem para o chat no VS Code (Copilot, Cline, Roo, Kilo) |
| `vscode/copilot-instructions.md` | Modelo **opcional**: copiar para `.github/copilot-instructions.md` na raiz do repo para o Copilot carregar as regras sozinho |
| `vscode/clinerules` | Modelo **opcional**: copiar para `.clinerules` na raiz do workspace para Cline/Roo/Kilo carregarem as regras sozinhos |

## Resumo das opções

| Ambiente | Custo | Como o agente recebe o kit |
|---|---|---|
| **Claude.ai** — chat simples (plano Free) | Grátis (com limite de mensagens) | Anexar os 3 arquivos do kit na 1ª mensagem + colar `BLOCO-CLAUDE-AI.txt` |
| **Claude.ai Projects** | Free com limites (~5 projetos, knowledge menor) · Pro ~US$ 20/mês libera ilimitado + RAG | Arquivos no *Project knowledge* + regras no *Project instructions*; todo chat novo já nasce com o agente |
| **VS Code + GitHub Copilot Free** | Grátis (2.000 conclusões + 50 chats/mês) | Abrir este repo e colar `BLOCO-VSCODE.txt`; opcional: copiar `vscode/copilot-instructions.md` para `.github/` na raiz → regras automáticas |
| **VS Code + Cline / Roo Code / Kilo Code** (BYOK) | Extensão grátis; modelo via chave própria — cota gratuita do Google AI Studio (Gemini) ou modelos free do OpenRouter = custo zero; API paga = centavos por uso | Abrir este repo e colar `BLOCO-VSCODE.txt`; opcional: copiar `vscode/clinerules` para a raiz → regras automáticas; o agente lê arquivos e executa comandos |

---

## Caminho 1 — Claude.ai com Projects (mais confortável)

1. Em claude.ai, abra **Projects → New project** (ex.: "Curadoria Prime — Editorial").
2. Em **Project knowledge**, suba os 3 arquivos: `README.md`, `CHECKLIST-EEAT-PUBLICO.md`, `ARTIGO-A-GUTENBERG.html` (e os anexos sensíveis do repo privado, quando houver).
3. Em **Project instructions**, cole a essência das regras (o texto de `vscode/copilot-instructions.md` serve igual): regra-mãe de honestidade, preço com data, afiliado sinalizado, antialucinação.
4. Todo chat iniciado dentro do projeto já herda arquivos + instruções — não precisa colar o bloco de novo.

> Projetos no plano Free têm limite de quantidade e de capacidade de arquivos; se a sua conta não exibir Projects ou estourar a cota, use o Caminho 2.

## Caminho 2 — Claude.ai chat simples (sempre funciona)

1. Novo chat → **anexe os 3 arquivos** do kit (no Free dá para anexar alguns arquivos por conversa).
2. Cole o conteúdo de `BLOCO-CLAUDE-AI.txt` como 1ª mensagem.
3. ⚠️ Não use o `BLOCO-URLS-PARA-PROMPT.txt` aqui: o chat do claude.ai não faz fetch confiável de URLs raw — por isso o bloco adaptado usa anexos.

## Caminho 3 — VS Code com GitHub Copilot (Free)

1. Instale a extensão **GitHub Copilot** no VS Code e entre com sua conta GitHub (plano Free: ~50 mensagens de chat/agente por mês + 2.000 conclusões).
2. Abra **este repositório** como workspace (`git clone` + File → Open Folder).
3. Cole `BLOCO-VSCODE.txt` no Copilot Chat como 1ª mensagem para ancorar a leitura dos arquivos do kit.
4. (Opcional, recomendado) Copie `PORTABILIDADE/vscode/copilot-instructions.md` para `.github/copilot-instructions.md` na raiz do repo — a partir daí o Copilot carrega as regras da casa automaticamente em todo chat, sem precisar colar nada.

## Caminho 4 — VS Code com Cline / Roo Code / Kilo Code (custo zero ou quase)

1. Instale a extensão **Cline** (ou Roo Code / Kilo Code) — grátis e open source.
2. Configure o provedor do modelo (BYOK):
   - **Custo zero:** chave gratuita do Google AI Studio (Gemini) ou modelos gratuitos do OpenRouter;
   - **Custo baixo:** chave pay-per-use (Anthropic, OpenRouter etc.) — você paga só os tokens usados, tipicamente centavos por sessão.
3. Abra este repo como workspace e cole `BLOCO-VSCODE.txt` como 1ª mensagem.
4. (Opcional, recomendado) Copie `PORTABILIDADE/vscode/clinerules` para `.clinerules` na raiz do workspace — Cline/Roo/Kilo passam a ler as regras da casa automaticamente.
5. Aqui o agente também consegue criar/editar arquivos HTML no repo e rodar comandos — bom para produção em lote.

## ⚠️ O que NÃO levar

Este repo público **não contém** handoff de sessão, roadmap de pautas, log-mestre nem packs de preço — e nenhum desses caminhos deve receber esses dados sem necessidade. Quando precisar deles em alguma ferramenta, anexe à parte (como no fluxo do Agent Mode) e prefira ambientes onde você controle a retenção de dados.
