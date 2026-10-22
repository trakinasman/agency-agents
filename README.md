# Seleção do Agency Agents

26 agentes escolhidos do [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents)
(commit `4e3ac3c`, 2026-10-19, licença MIT — ver `LICENSE`), de ~300. Copiados sem edição,
mantendo as pastas por área.

São agentes "com personalidade" (identidade, missão, fluxo, entregáveis, métricas). Mudam o tom e
o roteiro do Claude naquele papel; não trazem ferramentas novas. Nenhum traz script, e nenhum
duplica os agentes de engenharia do ECC já instalados em `~/.claude/agents/`.

**Esta pasta só guarda a seleção.** O Claude Code não carrega nada daqui sozinho.

## O que entrou, e para quê

| Área | Agentes | Uso pensado |
|---|---|---|
| Suporte | Support Responder, Analytics Reporter, Executive Summary Generator | Atendimento URA, chamados, relatórios para gestão |
| Vendas | Pipeline Analyst, Proposal Strategist, Outbound Strategist | CRMs (barbearias, previ, twenty, odoo) |
| Produto | Product Manager, Sprint Prioritizer, Feedback Synthesizer | Cards QD-xx, roadmap, feedback de usuários |
| Gestão de projetos | Senior Project Manager, Meeting Notes Specialist | Quebrar specs em tarefas, atas com decisões e pendências |
| Marketing | Instagram Curator, Content Creator, Email Marketing Strategist, SEO Specialist | Instagram, campanhas, e-mail via CRM, sites |
| Mídia paga | Paid Social Strategist, Tracking & Measurement Specialist | Meta/Instagram Ads, pixel e conversões |
| Finanças | Financial Analyst | Modelos e projeções (ex.: previ) |
| Segurança | Secrets & Credential Hygiene Engineer, Cloud Security Architect | Chave GCP commitada no `crm-q13`; IAM e Cloud Run |
| Engenharia (sem sobreposição com o ECC) | Data Engineer, SRE, FinOps Engineer, IT Service Manager, Minimal Change Engineer, Technical Writer | ETLs, confiabilidade e custo no GCP, processos ITIL do NOC, diffs mínimos, documentação |

Os campos `tools:` só existem em alguns; onde faltam, o agente herda todas as ferramentas da
sessão. Alguns exemplos citam mercados ou ferramentas dos EUA; o método vale igual.

## O que ficou de fora, e por quê

- **`marketing-carousel-growth-engine`**: publica sozinho no Instagram/TikTok via APIs externas e
  exige `GEMINI_API_KEY` e Playwright. Efeito externo demais para entrar sem decisão específica.
- **Marketing focado na China** (Douyin, WeChat, Xiaohongshu, Baidu, Bilibili…) e redes que não
  usamos (Reddit, podcast, livestream).
- **Engenharia que repete o ECC** (code reviewer, frontend, backend, database) **ou de outras
  stacks** (Drupal, WordPress, Solidity, mobile, Rust, Feishu…).
- **Áreas sem relação**: game dev, GIS, spatial computing, saúde, acadêmico, a maior parte de
  "specialized", integrações, design, testes e estratégia.
- **Scripts do repositório** (`install.sh`, `convert.sh`): instalam categorias inteiras; aqui a
  cópia é manual e seletiva.

## Instalar (quando decidir)

Copie os `.md` (sem as pastas) para `~/.claude/agents/` (todos os projetos) ou
`<projeto>/.claude/agents/` (um projeto) e abra uma sessão nova do Claude Code.
Chame pelo nome: *"use o Pipeline Analyst para analisar o funil do crm-barbearias"*.

## Atualizar a partir do original

Compare com o commit novo do upstream e copie de novo só os mesmos arquivos.
