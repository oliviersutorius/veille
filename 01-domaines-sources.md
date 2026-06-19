# Domaines de Veille et Sources

## 1. Domaines prioritaires

Les domaines sont classés par **impact stratégique** (haute → basse priorité).
Chaque domaine est assigné à un développeur référent, qui agrège et filtre pour l'équipe.

| # | Domaine | Périmètre | Référent suggéré |
|---|---|---|---|
| 1 | **Intelligence Artificielle / ML** | LLMs, RAG, agents, MLOps, edge AI | Voluntaire IA |
| 2 | **Cloud & Infrastructure** | Kubernetes, serverless, FinOps, multi-cloud | Ops/Platform |
| 3 | **Langages & Runtimes** | Php, React, Rust, Go, Python, WASM, nouveaux runtimes | Backend lead |
| 4 | **DevOps & Platform Engineering** | CI/CD, IaC, observabilité, developer portals | DevOps |
| 5 | **Sécurité** | Supply chain, SAST/DAST, secrets management, SBOM | Security champ |
| 6 | **Frameworks & Architecture** | microservices, event-driven, DDD, edge computing, symfony | Archi lead |
| 7 | **Frontend & Expérience Dev** | frameworks JS, design systems, tooling (Vite, Bun) | Frontend lead |
| 8 | **Data & Streaming** | data lakes, streaming (Kafka, Flink), data mesh | Data lead |

---

## 2. Sources par domaine

### Transversal (tous domaines — 20 min/semaine)

**Radars & synthèses**
- [ThoughtWorks Technology Radar](https://www.thoughtworks.com/radar) — référence trimestrielle
- [CNCF Landscape](https://landscape.cncf.io/) — écosystème cloud-native
- [State of DevOps Report](https://dora.dev/) — DORA metrics annuels
- [Stack Overflow Developer Survey](https://survey.stackoverflow.co/) — tendances annuelles
- [InfoQ](https://www.infoq.com/) — articles et mini-books de qualité

**Newsletters hebdomadaires** (5 min chacune)
- [TLDR Tech](https://tldr.tech/) — digest quotidien condensé
- [Pointer.io](https://www.pointer.io/) — articles pour engineering leaders
- [The Pragmatic Engineer](https://newsletter.pragmaticengineer.com/) — engineering de qualité (payant, mutualisable)

---

### Domaine 1 — Intelligence Artificielle / ML

| Type | Source | Fréquence |
|---|---|---|
| Blog | [Anthropic Research](https://www.anthropic.com/research) | Hebdo |
| Blog | [OpenAI Blog](https://openai.com/blog) | Hebdo |
| Blog | [Hugging Face Blog](https://huggingface.co/blog) | Hebdo |
| Newsletter | [The Batch (Andrew Ng)](https://www.deeplearning.ai/the-batch/) | Hebdo |
| Newsletter | [AI Tidbits](https://www.aitidbits.ai/) | Hebdo |
| Podcast | [Latent Space](https://www.latent.space/podcast) | Bi-hebdo |
| Podcast | [Practical AI](https://changelog.com/practicalai) | Hebdo |
| GitHub | [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) | Mensuel |
| Conférence | NeurIPS, ICML, MLSys | Annuel |
| Radar | [a16z AI Canon](https://a16z.com/ai-canon/) | Trimestriel |

---

### Domaine 2 — Cloud & Infrastructure

| Type | Source | Fréquence |
|---|---|---|
| Blog | [AWS What's New](https://aws.amazon.com/new/) | Hebdo |
| Blog | [Google Cloud Blog](https://cloud.google.com/blog) | Hebdo |
| Blog | [Kelsey Hightower (X/GitHub)](https://github.com/kelseyhightower) | Ponctuel |
| Newsletter | [Last Week in Kubernetes](https://lwkd.info/) | Hebdo |
| Newsletter | [CloudSecList](https://cloudseclist.com/) | Hebdo |
| Podcast | [Kubernetes Podcast (Google)](https://kubernetespodcast.com/) | Hebdo |
| Podcast | [Cloud Native Podcast](https://cloudnativepodcast.com/) | Hebdo |
| Conférence | KubeCon, re:Invent, Google Cloud Next | Annuel |
| Radar | [CNCF Annual Survey](https://www.cncf.io/reports/) | Annuel |

---

### Domaine 3 — Langages & Runtimes

| Type | Source | Fréquence |
|---|---|---|
| Blog | [PHP.net News](https://www.php.net/archive/2024.php) | Mensuel |
| Blog | [Stitcher.io (Brent Roose)](https://stitcher.io/) | Hebdo |
| Blog | [PHP Watch](https://php.watch/) | Hebdo |
| Blog | [Rust Blog](https://blog.rust-lang.org/) | Mensuel |
| Blog | [Go Blog](https://go.dev/blog/) | Mensuel |
| Blog | [Armin Ronacher](https://lucumr.pocoo.org/) | Ponctuel |
| Newsletter | [PHP Weekly](https://www.phpweekly.com/) | Hebdo |
| Newsletter | [Rust Weekly](https://this-week-in-rust.org/) | Hebdo |
| Newsletter | [Golang Weekly](https://golangweekly.com/) | Hebdo |
| Newsletter | [Python Weekly](https://www.pythonweekly.com/) | Hebdo |
| Podcast | [PHP Internals News](https://phpinternals.news/) | Hebdo |
| Podcast | [PHP Roundtable](https://phproundtable.com/) | Mensuel |
| Podcast | [Software Engineering Daily](https://softwareengineeringdaily.com/) | Quotidien |
| GitHub | [PHP RFC Watch](https://php-rfc-watch.beberlei.de/) | Mensuel |
| Conférence | PHPConf, ForumPHP (AFUP), RustConf, GopherCon, PyCon | Annuel |

---

### Domaine 4 — DevOps & Platform Engineering

| Type | Source | Fréquence |
|---|---|---|
| Blog | [Martin Fowler](https://martinfowler.com/) | Mensuel |
| Blog | [Gergely Orosz (Uber)](https://blog.pragmaticengineer.com/) | Hebdo |
| Blog | [Charity Majors](https://charity.wtf/) | Mensuel |
| Newsletter | [DevOps Weekly](https://www.devopsweekly.com/) | Hebdo |
| Newsletter | [Platform Engineering Weekly](https://platformweekly.com/) | Hebdo |
| Podcast | [Ship It! (Changelog)](https://changelog.com/shipit) | Hebdo |
| Podcast | [On Call Me Maybe](https://oncallmemaybe.com/) | Mensuel |
| GitHub | [awesome-platform-engineering](https://github.com/shospodarets/awesome-platform-engineering) | Mensuel |
| Conférence | DevOpsDays, Platform Engineering Conf | Annuel |

---

### Domaine 5 — Sécurité

| Type | Source | Fréquence |
|---|---|---|
| Blog | [Krebs on Security](https://krebsonsecurity.com/) | Hebdo |
| Blog | [OWASP Blog](https://owasp.org/blog/) | Mensuel |
| Blog | [Snyk Security Research](https://snyk.io/blog/) | Hebdo |
| Newsletter | [tl;dr sec](https://tldrsec.com/) | Hebdo |
| Newsletter | [Risky Business](https://risky.biz/) | Hebdo |
| Podcast | [Darknet Diaries](https://darknetdiaries.com/) | Bi-mensuel |
| Podcast | [Security Now (TWiT)](https://twit.tv/shows/security-now) | Hebdo |
| GitHub | [OWASP Top 10](https://github.com/OWASP/Top10) | Trimestriel |
| Radar | [ENISA Threat Landscape](https://www.enisa.europa.eu/topics/cyber-threats/enisa-threat-landscape) | Annuel |

---

### Domaine 6 — Frameworks & Architecture

| Type | Source | Fréquence |
|---|---|---|
| Blog | [Symfony Blog](https://symfony.com/blog/) | Hebdo |
| Blog | [Symfony Live / SymfonyCasts](https://symfonycasts.com/blog) | Hebdo |
| Blog | [JoliCode Blog](https://jolicode.com/blog) | Mensuel |
| Blog | [Les-Tilleuls.coop Blog](https://les-tilleuls.coop/blog) | Mensuel |
| Blog | [Martin Fowler Patterns](https://martinfowler.com/articles/) | Mensuel |
| Blog | [Netflix Tech Blog](https://netflixtechblog.com/) | Mensuel |
| Blog | [Uber Engineering](https://eng.uber.com/) | Mensuel |
| Newsletter | [Symfony Weekly](https://www.symfony-news.com/) | Hebdo |
| Newsletter | [Software Design Weekly](https://softwaredesignweekly.com/) | Hebdo |
| Newsletter | [Architecture Notes](https://architecturenotes.co/) | Mensuel |
| Podcast | [Symfony Deconstructed](https://feeds.simplecast.com/XA_851k3) | Mensuel |
| Podcast | [CoRecursive](https://corecursive.com/) | Mensuel |
| GitHub | [Symfony Releases](https://github.com/symfony/symfony/releases) | Mensuel |
| GitHub | [API Platform](https://github.com/api-platform/api-platform) | Mensuel |
| Conférence | SymfonyLive Paris, SymfonyCon, Forum PHP (AFUP) | Annuel |
| Livre | [Symfony Best Practices](https://symfony.com/doc/current/best_practices.html) | Référence |
| Livre | [Designing Distributed Systems (O'Reilly)](https://www.oreilly.com/) | Référence |

---

### Domaine 7 — Frontend & Expérience Dev

| Type | Source | Fréquence |
|---|---|---|
| Blog | [web.dev (Google)](https://web.dev/blog/) | Hebdo |
| Blog | [Josh W. Comeau](https://www.joshwcomeau.com/) | Mensuel |
| Newsletter | [JavaScript Weekly](https://javascriptweekly.com/) | Hebdo |
| Newsletter | [CSS Weekly](https://css-weekly.com/) | Hebdo |
| Newsletter | [Frontend Focus](https://frontendfoc.us/) | Hebdo |
| Podcast | [Syntax](https://syntax.fm/) | Hebdo |
| GitHub | [State of JS](https://stateofjs.com/) | Annuel |

---

### Domaine 8 — Data & Streaming

| Type | Source | Fréquence |
|---|---|---|
| Blog | [Confluent Blog](https://www.confluent.io/blog/) | Hebdo |
| Blog | [Databricks Blog](https://www.databricks.com/blog) | Hebdo |
| Newsletter | [Data Engineering Weekly](https://www.dataengineeringweekly.com/) | Hebdo |
| Newsletter | [The Data Engineering Podcast](https://www.dataengineeringpodcast.com/) | Hebdo |
| Podcast | [Data Engineering Podcast](https://www.dataengineeringpodcast.com/) | Hebdo |
| Conférence | Data Council, Kafka Summit, Flink Forward | Annuel |

---

## 3. Règle d'or des sources

> **Moins c'est plus.** Mieux vaut 3 sources lues attentivement que 20 survolées.
> Chaque développeur choisit **au maximum 5 sources** dans son domaine + 2 sources transversales.
> Il désabonne sans regret ce qu'il ne lit plus.
