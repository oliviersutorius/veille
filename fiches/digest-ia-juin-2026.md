# Digest IA — Juin 2026

**Type :** Digest de veille mensuel
**Domaine :** Intelligence Artificielle / ML
**Auteur :** Claude (veille automatisée)
**Date :** 2026-06-08
**Usage :** Préparation Tech Talk

---

## Sujet 1 — Les agents IA sont devenus mainstream (et ça change l'architecture)

Le tournant est acté : les LLMs seuls ne sont plus le sujet. La valeur est dans les **systèmes agentiques** — des programmes qui ont des objectifs, une mémoire, un planning et des outils.

**Signaux concrets ce mois-ci :**
- **Google I/O (19 mai)** — lancement de **Gemini Spark**, agent personnel 24/7 intégré à Gmail, Calendar et ~30 outils tiers via MCP. Google pousse MCP comme protocole standard de connexion agents ↔ outils.
- **Amazon Bedrock AgentCore** — ajout de capacités de paiement autonome pour agents (via Stripe / Coinbase). Les agents peuvent consommer des APIs payantes sans intervention humaine.
- **Hermes Agent** (Nous Research) — 140 000 étoiles GitHub en 3 mois, modèle agent open source le plus utilisé sur OpenRouter.

**Angle Tech Talk :** *"Qu'est-ce qu'une architecture agentique concrètement, et pourquoi ça change la façon dont on conçoit nos backends ?"*

---

## Sujet 2 — RAG classique vs Agentic RAG vs GraphRAG

Le RAG classique (embed → store → retrieve → generate) est en train d'être supplanté :

- **Agentic RAG** : la récupération devient une **boucle**. L'agent décide quels outils de recherche appeler, quand, et combien de fois. Gains significatifs sur la précision vs RAG classique selon les benchmarks.
- **GraphRAG** : combine recherche vectorielle + graphes de connaissances. Précision annoncée jusqu'à 99% sur des corpus structurés (juridique, médical, documentation technique).
- **Tendance de fond** : les bases vectorielles standalone (Pinecone, Weaviate) perdent des parts au profit du **retrieval hybride** intégré dans les bases existantes — pgvector dans PostgreSQL en tête. Le Pulse Survey VentureBeat Q1 2026 note que l'intent retrieval hybride a triplé à 33,3%.

**Pertinence stack :** pgvector est en Adopt dans notre radar. Moment opportun pour évaluer si on passe d'un RAG classique à une approche agentique.

**Angle Tech Talk :** *"De RAG classique aux agents : ce qui change concrètement dans nos architectures"* (combiné avec Sujet 1 pour une présentation de 15 min)

---

## Sujet 3 — La guerre des LLMs open source s'accélère

Sorties majeures en mai-juin 2026 :

| Modèle | Éditeur | Point fort |
|---|---|---|
| **Qwen 3 235B-A22B** | Alibaba | Meilleur open source global (coding + raisonnement) |
| **Llama 4 Scout** | Meta | Contexte 10M tokens — une codebase entière en un prompt |
| **DeepSeek R1-0528** | DeepSeek | Raisonnement mathématique, leader sur les benchmarks maths |
| **Phi-4 Reasoning Vision** | Microsoft | Multimodal + raisonnement, 15B params seulement |
| **MiMo-V2.5-Pro** | Xiaomi | Spécialisé agents de coding, 42B actifs / 1T total |

**Signal clé :** un nouveau modèle sort en moyenne toutes les **3 jours**. Les abstractions (LangChain, LiteLLM, Ollama) prennent encore plus de valeur pour s'isoler de cette volatilité.

**Question ouverte pour l'équipe :** Avec Ollama en Trial dans notre radar, Llama 4 Scout ou Qwen 3 sont-ils prêts à remplacer un appel Claude API pour nos usages internes ?

---

## Sujet 4 — Claude Opus 4.8 et Anthropic

- **Claude Opus 4.8** sorti le 28 mai — capacités agentiques renforcées, meilleur sur les tâches de coding longue durée.
- Anthropic annonce un **run rate de 30 milliards de dollars**, croissance 80× en Q1 2026.
- Anthropic accuse DeepSeek, Moonshot et MiniMax de **distillation industrielle** via des milliers de comptes frauduleux pour extraire la connaissance de Claude. Point d'attention pour nos contrats d'utilisation des APIs.

---

## Recommandation Tech Talk

| Slot | Contenu | Durée |
|---|---|---|
| Présentation principale | Sujets 1 + 2 — *"De RAG classique aux agents : ce qui change dans nos architectures"* | 15 min |
| Sujet court | Sujet 3 — Tour d'horizon LLMs open source + question Ollama / Llama 4 Scout | 5 min |

---

## Sources

- [LLM News Today — June 2026](https://llm-stats.com/ai-news)
- [AI Model Release Timeline 2025–2026](https://aiflashreport.com/model-releases.html)
- [Top Agentic Frameworks 2026 — JetBrains](https://blog.jetbrains.com/pycharm/2026/06/top-agentic-frameworks-for-building-applications-2026/)
- [Agentic AI Week in Review May 19-23](https://www.digitalapplied.com/blog/agentic-ai-week-in-review-may-19-23-2026/)
- [The best open-source LLMs in 2026 — BentoML](https://www.bentoml.com/blog/navigating-the-world-of-open-source-large-language-models)
- [RAG is ending for agentic AI — VentureBeat](https://venturebeat.com/data/the-rag-era-is-ending-for-agentic-ai-a-new-compilation-stage-knowledge-layer-is-what-comes-next)
- [AI Agents don't need vector search anymore — Medium](https://buzzgrewal.medium.com/ai-agents-dont-need-vector-search-anymore-inside-the-agentic-search-stack-replacing-rag-in-2026-58efcabe4f6f)
