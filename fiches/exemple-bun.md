# Bun 1.x — Fiche d'Évaluation

**Domaine :** Frontend & Expérience Dev
**Auteur :** Marie Dupont
**Date d'évaluation :** 2026-05-20
**Version évaluée :** 1.1.20
**Statut radar proposé :** Trial

---

### 1. Présentation

**En une phrase :**
> Bun est un runtime JavaScript tout-en-un (exécuteur, bundler, test runner, package manager) écrit en Zig, conçu pour être 10 à 30× plus rapide que Node.js sur les opérations courantes.

**Problème résolu :**
> Nos builds frontend en CI prennent 4 min dont 45 sec pour `npm install`. Le temps développeur perdu sur les feedbacks lents de CI est estimé à 30 min/dev/jour.

**Alternatives connues :**
> - **Node.js 22** — standard de facto, compatibilité maximale, mais pas d'amélioration de performance significative
> - **Deno 2** — sécurité first, compatible Node API, bonnes performances mais moins rapide que Bun sur les benchmarks npm

---

### 2. Maturité Technique

| Critère | Score | Justification |
|---|---|---|
| Stabilité de l'API | 4/5 | Stable depuis v1.0 (sept 2023), quelques edge cases sur addons natifs |
| Qualité documentation | 5/5 | Excellente, claire, avec exemples pratiques et migration guide |
| Couverture de tests | 4/5 | Suite de tests publique solide, CI visible sur GitHub |
| Fréquence des releases | 5/5 | Releases quasiment hebdomadaires avec changelogs détaillés |
| Gestion breaking changes | 4/5 | Semver respecté depuis v1.0, breaking changes annoncés |
| **Score maturité** | **22/25** | |

**Version stable depuis :** Septembre 2023 (v1.0)
**Dernière release majeure :** v1.1 — amélioration des workers, bundler stabilisé
**Roadmap publique :** Oui — [github.com/oven-sh/bun/milestones](https://github.com/oven-sh/bun/milestones)

---

### 3. Communauté & Écosystème

| Critère | Valeur | Commentaire |
|---|---|---|
| Étoiles GitHub | 72k+ | Croissance régulière |
| Issues ouvertes / fermées | 3.2k / 28k | Ratio sain, équipe réactive |
| Contributeurs actifs (90j) | 45+ | Core team + communauté |
| Âge du projet | 3 ans | Lancé 2021, public 2022 |
| Dernière activité | Hier | Très actif |
| Questions Stack Overflow | 4k+ | Montée en puissance |
| Licence | MIT | Totalement libre |

**Utilisé en production par :** Vercel, Supabase, Expo, PlanetScale, plusieurs startups YC

**Backing :** Oven Inc. (levée de fonds Series A, équipe dédiée)

---

### 4. Applicabilité à notre contexte

**Use cases identifiés :**
1. **Pipeline CI/CD** — remplacer `npm install + node build` → gain estimé 60-70% — impact : fort
2. **Test runner** — remplacer Jest par `bun test` → syntaxe identique, 10x plus rapide — impact : fort
3. **Scripts utilitaires** — écrire les scripts de maintenance en TypeScript natif sans compilation — impact : moyen

**Compatibilité stack :**

| Élément | Compatible ? | Notes |
|---|---|---|
| TypeScript | Oui | Exécution native sans transpilation |
| React 19 | Oui | Framework-agnostique |
| GitHub Actions | Oui | Image Docker officielle disponible |
| PostgreSQL (pg) | Oui | Driver compatible |
| Vite | Partiel | Bun bundler est une alternative, Vite reste utilisable |

**POC possible en :** 1 semaine (migration CI d'un projet pilote)

---

### 5. Risques

| Risque | Probabilité | Impact | Mitigation |
|---|---|---|---|
| Addons natifs Node incompatibles | Faible | Élevé | Vérifier node_modules — notre stack n'utilise pas d'addons C++ |
| Bun Ltd change de stratégie | Faible | Moyen | MIT license, fork possible si besoin |
| Bug dans runtime | Faible | Élevé | Tests de régression obligatoires lors de la migration |
| Courbe d'apprentissage | Très faible | Faible | API identique à Node.js |

**CVE connus :** Aucun critique à ce jour (vérifié 2026-05-20)

---

### 6. Coût d'Adoption

| Profil | Temps pour être opérationnel |
|---|---|
| Dev junior | 1h (API Node compatible) |
| Dev senior | 30 min |
| Équipe complète | 0 (migration transparente pour devs) |

| Dimension | Estimation | Détails |
|---|---|---|
| Migration CI | 1 jour | Modifier Dockerfile CI + tester les pipelines |
| Migration test runner | 2 jours | Remplacer jest.config → bun, corriger edge cases |
| Documentation équipe | 0.5 jour | Update CONTRIBUTING.md |
| **Total** | **3.5 jours** | 1 développeur |

**Coût récurrent :** 0 (open source)

---

### 7. Expérimentation

**POC réalisé :** Oui — 2026-05-18

**Résultats :**
- `npm install` → `bun install` : **de 45 sec à 8 sec** (-82%)
- `jest` → `bun test` sur notre suite (450 tests) : **de 23 sec à 4 sec** (-83%)
- Aucune régression détectée sur le projet `frontend-dashboard`

**Repo POC :** `git.internal/team/poc-bun-ci`

---

### 8. Verdict

| Dimension | Score pondéré |
|---|---|
| Maturité | 5.5/6.25 |
| Communauté | 0.9/1 |
| Applicabilité | 1.4/1.5 |
| Risques (inversé) | 0.65/0.75 |
| Coût d'adoption | 0.45/0.5 |
| **Total** | **8.9/10** |

**Placement proposé : Trial** *(score suggère Adopt, mais on préfère 1 trimestre de Trial en prod)*

**Justification :** Gains de performance spectaculaires confirmés en POC (-80% sur CI). Compatibilité avec notre stack excellente. Risque d'incompatibilité addons natifs nul dans notre contexte. La seule raison de ne pas passer directement en Adopt est le manque de recul en production sur nos projets spécifiques.

**Prochaine action :** Migrer le pipeline CI de `frontend-dashboard` et `api-gateway` (2 projets, 1 sprint). Réévaluer pour passage en Adopt en Q3 2026.

**À réévaluer le :** 2026-09-07

---

### 9. Références

| Type | Lien |
|---|---|
| Site officiel | https://bun.sh |
| GitHub | https://github.com/oven-sh/bun |
| Benchmark officiel | https://bun.sh/bench |
| Talk JSConf 2023 | [youtube] "Bun: a fast JavaScript runtime" |
| Comparatif Node vs Bun | https://blog.logrocket.com/bun-vs-node-js/ |

---

### 10. Historique

| Date | Évaluateur | Statut | Note |
|---|---|---|---|
| 2026-05-20 | Marie Dupont | Trial | Première évaluation avec POC |
