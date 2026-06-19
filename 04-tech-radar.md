# Tech Radar de l'Équipe

> Inspiré du [ThoughtWorks Technology Radar](https://www.thoughtworks.com/radar).
> Mis à jour trimestriellement. Version courante : **Q2 2026**.
> Dernière mise à jour : 2026-06-08 | Prochain review : **2026-09-05**

---

## Les 4 anneaux — Définitions

| Anneau | Définition | Action attendue |
|---|---|---|
| **ADOPT** | Technologie mature, éprouvée, recommandée pour un usage en production. Nous la choisissons par défaut pour les nouveaux projets relevant de son domaine. | Utiliser sans hésitation |
| **TRIAL** | Technologie prometteuse, avec un ou plusieurs POC positifs. Nous encourageons son utilisation sur des projets non critiques pour acquérir de l'expérience. | Tester sur un vrai projet |
| **ASSESS** | Technologie intéressante qui mérite notre attention. Pas encore de POC, mais nous la surveillons activement et invitons les curieux à explorer. | Explorer, lire, faire des POC perso |
| **HOLD** | Technologie que nous déconseillons d'adopter aujourd'hui. Soit trop immature, soit dépassée, soit trop risquée dans notre contexte. Les projets existants peuvent rester dessus, mais on n'en démarre pas de nouveau. | Ne pas démarrer de nouveaux projets |

---

## Radar Q2 2026

> Format : Nom — [description courte] — *ajouté/déplacé depuis [anneau précédent] en [trimestre]*

---

### LANGAGES & FRAMEWORKS

#### ADOPT

- **PHP 8.3+** — langage principal du backend, JIT compiler, enums, fibers, support officiel jusqu'en 2027
- **Symfony 7.x** — framework PHP principal, LTS 4 ans, architecture hexagonale, injection de dépendances mature
- **Symfony Messenger** — bus de messages async natif Symfony, gestion des queues et retry sans librairie tierce
- **Doctrine ORM 3** — ORM PHP de référence, migrations versionnées, support complet PostgreSQL/MySQL
- **TypeScript** — typage statique pour JavaScript, standard de facto pour nos projets frontend et backend Node.js
- **Python 3.12+** — langage principal pour le data engineering et les scripts ML/IA
- **Go 1.22+** — services à haute performance, outillage interne
- **React 19** — framework UI principal, avec Server Components stabilisés
- **FastAPI** — framework Python API REST/async, documentation OpenAPI automatique

#### TRIAL

- **API Platform 3.x** — framework REST/GraphQL/JSON-LD sur Symfony, génération automatique d'APIs conformes aux standards — *évalué Q2 2026*
- **Pest PHP 3** — framework de tests BDD pour PHP, syntaxe expressive, couverture de code et architecture tests — *évalué Q2 2026*
- **Bun 1.x** — runtime JS 10-30x plus rapide que Node pour build/test en CI — *évalué Q2 2026*
- **Astro 4** — framework frontend orienté contenu, excellent Time-to-Interactive — *évalué Q1 2026*
- **Hono** — framework web ultra-léger pour edge computing et WASM — *évalué Q2 2026*

#### ASSESS

- **FrankenPHP** — runtime PHP moderne embarqué dans Caddy, workers persistants, HTTP/3, Early Hints — *sous surveillance*
- **Symfony AssetMapper** — alternative no-build à Webpack/Vite pour projets Symfony full-stack — *sous surveillance*
- **Rust** — performance native pour composants critiques, courbe d'apprentissage élevée — *sous surveillance*
- **Gleam** — langage fonctionnel sur BEAM/Erlang, typage fort, pour systèmes distribués
- **Effect-TS** — gestion des effets de bord en TypeScript, paradigme fonctionnel

#### HOLD

- **PHP < 8.1** — pas d'enums, pas de fibers, hors support sécurité — migrer vers 8.3+
- **Symfony < 6.x** — versions hors support LTS, ne pas démarrer de nouveaux projets dessus
- **CoffeeScript** — remplacé par TypeScript
- **Flow (Facebook)** — remplacé par TypeScript
- **jQuery** — remplacé par frameworks modernes, sauf contrainte legacy

---

### INFRASTRUCTURE & CLOUD

#### ADOPT

- **Kubernetes 1.30+** — orchestration de conteneurs, standard pour tous nos déploiements
- **Terraform 1.x** — IaC déclaratif, utilisé pour toute la gestion d'infra cloud
- **GitHub Actions** — CI/CD principal, pipelines as code
- **Docker** — containerisation, runtime OCI standard
- **AWS (EKS, RDS, S3, SQS)** — cloud provider principal

#### TRIAL

- **OpenTofu** — fork Terraform open-source post-changement de licence BSL — *migration envisagée*
- **Crossplane** — gestion d'infrastructure Kubernetes-native, alternative à Terraform pour le cloud — *POC en cours*
- **Cilium CNI** — networking Kubernetes basé eBPF, remplacement de kube-proxy — *testé en staging*

#### ASSESS

- **Nomad** — orchestrateur HashiCorp plus simple que K8s pour workloads simples
- **Fly.io** — platform-as-a-service pour déploiements edge rapides
- **WASM sur edge** — exécution de fonctions WASM sur CDN (Cloudflare Workers, Fastly Compute)
- **Dagger** — pipelines CI/CD comme du code Go/Python/TypeScript, portables

#### HOLD

- **Ansible pour provisioning cloud** — remplacé par Terraform/Crossplane (garder pour config management OS)
- **Monolithes serverless AWS Lambda** — coûts et cold starts problématiques > 1k req/s
- **Helm 2** — remplacé par Helm 3

---

### INTELLIGENCE ARTIFICIELLE & ML

#### ADOPT

- **Claude API (Anthropic)** — LLM principal pour nos features IA, excellent rapport qualité/prix
- **LangChain / LangGraph** — orchestration d'agents LLM, RAG pipelines
- **pgvector** — stockage de vecteurs dans PostgreSQL, simplifie l'architecture RAG

#### TRIAL

- **Ollama** — inférence de LLMs en local (Llama, Mistral), pour dev et données sensibles — *testé Q2 2026*
- **DSPy** — framework de programmation LLM déclaratif, alternatives aux prompt templates manuels
- **LlamaIndex** — RAG avancé, indexation multi-sources, alternative à LangChain

#### ASSESS

- **OpenAI Realtime API** — API voix temps-réel pour features conversationnelles
- **MLflow** — tracking d'expériences ML, model registry, serving
- **Instructor** — extraction de données structurées depuis LLMs (Python)
- **Claude Computer Use** — automatisation d'interfaces via vision + IA

#### HOLD

- **AutoML sans supervision** — résultats peu prévisibles sans expertise domaine
- **GPT-3 / modèles < 2024** — remplacés par modèles récents plus performants

---

### DEVOPS & OBSERVABILITÉ

#### ADOPT

- **OpenTelemetry** — standard d'observabilité pour traces, métriques, logs
- **Grafana + Prometheus** — stack de monitoring et alerting de référence
- **ArgoCD** — déploiements GitOps sur Kubernetes
- **SOPS + age** — chiffrement de secrets dans Git
- **Renovate** — mise à jour automatique des dépendances (remplace Dependabot)

#### TRIAL

- **Temporal.io** — orchestration de workflows durables, fiables — *POC sur pipeline de facturation*
- **Grafana Loki** — centralisation de logs sans indexation full-text, coût réduit vs Elasticsearch
- **Buildkite** — CI/CD performant avec agents auto-hébergés — *évaluation en cours*

#### ASSESS

- **Dagger** — pipelines CI comme du code, portables entre environnements
- **Earthly** — builds reproductibles avec syntaxe Dockerfile + Makefile
- **VictoriaMetrics** — stockage métriques haute performance, alternative Prometheus
- **Beyla (eBPF)** — instrumentation auto-magique sans SDK OpenTelemetry

#### HOLD

- **Jenkins** — complexité opérationnelle trop élevée, remplacé par GitHub Actions
- **Ansible Tower** — remplacé par ArgoCD pour le déploiement applicatif
- **Nagios** — remplacé par Grafana/Prometheus

---

### SÉCURITÉ

#### ADOPT

- **Trivy** — scanner de vulnérabilités CVE pour images Docker et IaC
- **HashiCorp Vault** — gestion centralisée des secrets
- **Dependabot / Renovate** — alertes et mises à jour automatiques des dépendances
- **OWASP ZAP** — DAST sur les APIs en CI/CD
- **SBOM (CycloneDX)** — génération de Software Bill of Materials pour supply chain

#### TRIAL

- **Semgrep** — SAST avec règles custom, intégration CI facile — *en déploiement*
- **Falco** — détection d'anomalies runtime dans Kubernetes
- **Sigstore / Cosign** — signature et vérification d'images de conteneurs

#### ASSESS

- **Tetragon (Cilium)** — security enforcement eBPF dans Kubernetes
- **OpenFGA** — système d'autorisation fine-grained (Google Zanzibar open-source)
- **SLSA framework** — niveaux de confiance pour la supply chain logicielle

#### HOLD

- **Secrets hardcodés** — politique zéro tolérance, audit automatique en CI
- **CVEs non patchés > 90 jours** — politique SLA obligatoire

---

### DATA & STREAMING

#### ADOPT

- **PostgreSQL 16+** — base de données relationnelle principale
- **Redis 7+** — cache distribué, queues légères
- **Kafka** — streaming d'événements pour architectures event-driven
- **dbt** — transformation de données SQL versionnée

#### TRIAL

- **ClickHouse** — OLAP colonnaire ultra-rapide pour analytics temps réel — *POC analytics dashboard*
- **Apache Iceberg** — format de table open pour data lakehouse

#### ASSESS

- **Redpanda** — alternative Kafka sans ZooKeeper, compatible API Kafka
- **RisingWave** — base de données streaming SQL, alternative Flink pour certains cas
- **DuckDB** — OLAP embarqué, excellent pour analytics locaux et notebooks

#### HOLD

- **MongoDB pour données relationnelles** — utiliser PostgreSQL sauf besoin documentaire démontré
- **Hadoop / HDFS** — architecture dépassée pour nos volumes de données

---

## Historique des changements

| Trimestre | Technologie | Mouvement | Raison |
|---|---|---|---|
| Q2 2026 | PHP 8.3+ | Nouveau | Ajout au radar — langage principal backend |
| Q2 2026 | Symfony 7.x | Nouveau | Ajout au radar — framework PHP principal |
| Q2 2026 | Symfony Messenger | Nouveau | Ajout au radar — bus de messages async natif |
| Q2 2026 | Doctrine ORM 3 | Nouveau | Ajout au radar — ORM PHP de référence |
| Q2 2026 | API Platform 3.x | Nouveau | Ajout au radar — Trial, génération d'APIs Symfony |
| Q2 2026 | Pest PHP 3 | Nouveau | Ajout au radar — Trial, alternative à PHPUnit |
| Q2 2026 | FrankenPHP | Nouveau | Ajout au radar — Assess, runtime PHP nouvelle génération |
| Q2 2026 | PHP < 8.1 | Nouveau | Hold — versions hors support sécurité |
| Q2 2026 | Bun 1.x | Assess → Trial | POC CI : -65% build time confirmé |
| Q2 2026 | OpenTofu | Hold → Trial | Changement licence BSL Terraform |
| Q2 2026 | Ollama | Assess → Trial | Besoin données sensibles sans cloud |
| Q2 2026 | LangChain | Trial → Adopt | Usage stable sur 3 projets |
| Q1 2026 | Jenkins | Adopt → Hold | Migration GitHub Actions complète |
| Q1 2026 | Astro 4 | Assess → Trial | POC site docs positif |

---

## Processus de contribution

### Proposer une nouvelle technologie

1. Poster dans `#veille-tech` avec le tag `[RADAR-PROPOSE]`
2. Remplir la fiche d'évaluation (`02-fiche-evaluation.md`)
3. Présenter au prochain Tech Talk ou Brown Bag
4. Vote de l'équipe lors du review trimestriel

### Proposer un déplacement

1. Poster dans `#veille-tech` avec `[RADAR-MOVE] TechnoX : Trial → Adopt`
2. Justifier avec données factuelles (usage en production, incidents, benchmarks)
3. Vote lors du review trimestriel

### Règles de gouvernance

| Règle | Détail |
|---|---|
| **Quorum** | Minimum 50% de l'équipe présente pour valider un changement |
| **Adopt** | Requiert 80% d'accord (décision structurante) |
| **Trial / Assess** | Requiert 60% d'accord |
| **Hold** | Requiert 60% d'accord (protège contre effet de mode) |
| **Urgence** | Un tech lead peut placer en Hold immédiatement si risque sécurité avéré |

---

## Radar visuel

> Générer le visuel interactif sur : https://radar.thoughtworks.com
> Ou utiliser le template JSON ci-dessous avec l'outil Build Your Own Radar de ThoughtWorks.

```json
{
  "name": "Team Tech Radar Q2 2026",
  "quadrants": [
    "Langages & Frameworks",
    "Infrastructure & Cloud",
    "IA & ML",
    "DevOps, Sécurité & Data"
  ],
  "rings": [
    {"name": "ADOPT", "color": "#5BA300"},
    {"name": "TRIAL", "color": "#009EB0"},
    {"name": "ASSESS", "color": "#C7BA00"},
    {"name": "HOLD", "color": "#E09B96"}
  ],
  "entries": [
    {"label": "PHP 8.3+", "quadrant": 0, "ring": 0, "active": true, "moved": 0},
    {"label": "Symfony 7.x", "quadrant": 0, "ring": 0, "active": true, "moved": 0},
    {"label": "Symfony Messenger", "quadrant": 0, "ring": 0, "active": true, "moved": 0},
    {"label": "Doctrine ORM 3", "quadrant": 0, "ring": 0, "active": true, "moved": 0},
    {"label": "TypeScript", "quadrant": 0, "ring": 0, "active": true, "moved": 0},
    {"label": "API Platform 3.x", "quadrant": 0, "ring": 1, "active": true, "moved": 0},
    {"label": "Pest PHP 3", "quadrant": 0, "ring": 1, "active": true, "moved": 0},
    {"label": "Bun 1.x", "quadrant": 0, "ring": 1, "active": true, "moved": 1},
    {"label": "FrankenPHP", "quadrant": 0, "ring": 2, "active": true, "moved": 0},
    {"label": "Rust", "quadrant": 0, "ring": 2, "active": true, "moved": 0},
    {"label": "PHP < 8.1", "quadrant": 0, "ring": 3, "active": false, "moved": 0},
    {"label": "Kubernetes", "quadrant": 1, "ring": 0, "active": true, "moved": 0},
    {"label": "OpenTofu", "quadrant": 1, "ring": 1, "active": true, "moved": 1},
    {"label": "Dagger", "quadrant": 1, "ring": 2, "active": true, "moved": 0},
    {"label": "Claude API", "quadrant": 2, "ring": 0, "active": true, "moved": 0},
    {"label": "Ollama", "quadrant": 2, "ring": 1, "active": true, "moved": 1},
    {"label": "OpenAI Realtime", "quadrant": 2, "ring": 2, "active": true, "moved": 0},
    {"label": "OpenTelemetry", "quadrant": 3, "ring": 0, "active": true, "moved": 0},
    {"label": "Temporal.io", "quadrant": 3, "ring": 1, "active": true, "moved": 0},
    {"label": "Jenkins", "quadrant": 3, "ring": 3, "active": false, "moved": -1}
  ]
}
```

---

## Archives

| Version | Fichier |
|---|---|
| Q1 2026 | [archives/radar-2026-Q1.md](archives/radar-2026-Q1.md) |

---

*Tech Radar v1.0 — Prochain review : semaine du 2026-09-07*
