# Plataforma de IA vertical para marketing e vendas (multi-região)

> Estudo de caso do [portfólio de soluções de Jon Timoteo](https://github.com/jontimoteo-programmer/ai-solutions-portfolio) · Arquiteto de Soluções de IA & Cloud · Engenheiro Full Stack Sênior

| Área | Período | Status |
|---|---|---|
| Inteligência Artificial & Agentes | jan/2026 – set/2026 | Entregue |

Plataforma de IA por assinatura em produção em duas regiões (Brasil e Austrália), com 8 agentes especialistas por área de negócio, 12 bases de conhecimento curadas e ferramentas que geram relatórios gerenciais, carrosséis, vídeos narrados e fluxogramas, além de leitura da presença digital do usuário para personalizar as respostas.

Arquitetura: dezenas de serviços em containers, duas regiões isoladas sobre banco central (PostgreSQL + pgvector), API em FastAPI atrás de proxy reverso, microsserviços acessados por proxy JWT, gateway de pagamento que transforma a compra em conta ativa (webhooks Stripe → provisionamento → Meta CAPI server-side).

Chat com contexto de até 1M de tokens e roteamento por tipo de arquivo: áudio para Whisper local, imagem e PDF escaneado para modelo de visão com OCR, planilha para Pandas. Pipeline de RAG com humano no loop em 7 fases (mineração, limpeza, refinamento por LLM, quarentena, curadoria e injeção multi-região).

Segurança em camadas, da borda à aplicação e ao prompt, com detecção e bloqueio automatizados de tráfego malicioso e limite de consumo por usuário.

P&D: dataset de fine-tuning com 8.323 exemplos e pipeline documentado; arquitetura de agentes com ReAct e MCP.

Decisões de arquitetura: microsserviços especialistas atrás de um core, com a camada de IA acessada por proxy JWT em vez de embutida na aplicação; regiões isoladas sobre banco central, para escalar país novo sem duplicar operação; custo de IA tratado como requisito de projeto (teto por usuário, escolha de modelo por benchmark de custo × qualidade e compressão de contexto); cascata de provedores com failover, depois de uma indisponibilidade de API em produção.

Stack: Python, FastAPI, Node.js, React, PostgreSQL + pgvector, DeepSeek, OpenRouter, Ollama, faster-whisper, FFmpeg, Docker, Stripe.

**Competências:** Inteligência Artificial (IA) · Arquitetura de Soluções · Python · FastAPI · RAG

---

Projeto de cliente descrito por setor, sem nome, números identificáveis ou código proprietário. Veja todos os 79 projetos no [índice do portfólio](https://github.com/jontimoteo-programmer/ai-solutions-portfolio).
