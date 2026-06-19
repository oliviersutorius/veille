# Veille Technologique

Lance une veille technologique sur les **2 dernières semaines** couvrant les 8 domaines du radar de l'équipe.

## Instructions

1. Lire `01-domaines-sources.md` pour connaître les domaines et sources à surveiller
2. Lire `04-tech-radar.md` pour connaître l'état courant du radar (technologies en ADOPT/TRIAL/ASSESS/HOLD)
3. Lancer des recherches web **en parallèle** sur les 8 domaines :
   - Intelligence Artificielle / ML (LLMs, RAG, agents, LangChain, Claude API, Ollama)
   - Cloud & Infrastructure (Kubernetes, AWS EKS, OpenTofu, Crossplane, Cilium)
   - Langages & Runtimes (PHP, Symfony, TypeScript, Go, Python, Bun, Rust)
   - DevOps & Platform Engineering (GitHub Actions, ArgoCD, OpenTelemetry, Temporal, Grafana)
   - Sécurité (supply chain, CVEs, SAST/DAST, secrets, SBOM)
   - Frameworks & Architecture (Symfony, API Platform, microservices, event-driven)
   - Frontend & Expérience Dev (React 19, TypeScript, Vite, Bun, design systems)
   - Data & Streaming (Kafka, ClickHouse, PostgreSQL, dbt, Apache Iceberg)
4. Compiler les résultats en français, organisés par domaine
5. Identifier les signaux susceptibles d'impacter le radar (🔔) et les alertes sécurité (⚠️)
6. Produire un tableau récapitulatif des mouvements radar potentiels
7. **Enregistrer le résultat dans `infos/veille_YYYY-MM-DD.html`** (date du jour au format ISO 8601) avec un rendu HTML propre et lisible

## Format du fichier HTML

Le fichier HTML doit :
- Avoir un en-tête avec la date, le titre "Veille Technologique" et le périmètre (2 semaines)
- Utiliser des sections `<section>` par domaine avec une `<h2>` pour chaque domaine
- Mettre en avant les signaux 🔔 et alertes ⚠️ avec des styles visuels distincts (couleurs)
- Inclure un tableau récapitulatif des signaux radar en fin de document
- Avoir une section "Sources" avec les liens cliquables
- Être autonome (CSS inline, pas de dépendances externes)
- Utiliser une police lisible et un contraste élevé

## Périmètre temporel

Toujours rechercher les **2 dernières semaines** à partir de la date du jour (variable `$CURRENT_DATE` disponible dans le contexte).
