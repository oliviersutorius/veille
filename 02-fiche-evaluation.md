# Fiche d'Évaluation Technologique

> Durée de remplissage estimée : **45 min à 1h30** selon la profondeur souhaitée.
> Une fiche = une technologie. Une fiche incomplète vaut mieux que pas de fiche.

---

## Template — Fiche d'Évaluation

```
# [NOM DE LA TECHNOLOGIE] — Fiche d'Évaluation

**Domaine :** [IA / Cloud / Langage / DevOps / Sécurité / Architecture / Frontend / Data]
**Auteur :** [Prénom Nom]
**Date d'évaluation :** [YYYY-MM-DD]
**Version évaluée :** [ex: 2.1.0 / latest / N/A]
**Statut radar proposé :** [ ] Adopt  [ ] Trial  [ ] Assess  [ ] Hold
```

---

### 1. Présentation (5 min)

**En une phrase :**
> [Décrire la technologie en une phrase, comme si on l'expliquait à quelqu'un qui n'en a jamais entendu parler]

**Problème résolu :**
> [Quel problème concret cette technologie adresse-t-elle ? Qui en souffre aujourd'hui dans notre équipe ?]

**Alternatives connues :**
> [Lister 2-3 alternatives directes avec une différenciation courte]
> - Alternative A — [différence clé]
> - Alternative B — [différence clé]

---

### 2. Maturité Technique

| Critère | Score (1-5) | Justification |
|---|---|---|
| Stabilité de l'API/interface | /5 | |
| Qualité de la documentation | /5 | |
| Couverture de tests de la lib | /5 | |
| Fréquence des releases | /5 | |
| Gestion des breaking changes | /5 | |
| **Score maturité** | **/25** | |

**Version stable depuis :** [date ou "pas encore stable"]
**Dernière release majeure :** [date + changelog notable]
**Roadmap publique :** [ ] Oui — [lien]  [ ] Non  [ ] Partielle

---

### 3. Communauté & Écosystème

| Critère | Valeur | Commentaire |
|---|---|---|
| Étoiles GitHub | | |
| Issues ouvertes / fermées | / | ratio actif ? |
| Contributeurs actifs (90j) | | |
| Âge du projet | | |
| Dernière activité GitHub | | |
| Questions Stack Overflow | | |
| Forks notables | | |
| Licence | | [MIT / Apache / GPL / propriétaire] |

**Qui l'utilise en production ?**
> [Citer 3-5 entreprises connues avec liens si possible]

**Backing organisationnel :**
> [ ] CNCF (sandbox / incubating / graduated)
> [ ] Fondation Apache
> [ ] Éditeur commercial (nom : _______)
> [ ] Communauté indépendante
> [ ] Projet abandonné / archivé

---

### 4. Applicabilité à notre contexte

**Use cases identifiés chez nous :**
> [Décrire 1-3 cas d'usage concrets dans notre stack actuelle]
> 1. [Use case A] — impact estimé : [fort / moyen / faible]
> 2. [Use case B] — impact estimé : [fort / moyen / faible]

**Compatibilité avec notre stack :**

| Élément de stack | Compatible ? | Notes |
|---|---|---|
| [Langage principal] | [ ] Oui [ ] Non [ ] Partiel | |
| [Cloud provider] | [ ] Oui [ ] Non [ ] Partiel | |
| [CI/CD actuel] | [ ] Oui [ ] Non [ ] Partiel | |
| [BDD actuelle] | [ ] Oui [ ] Non [ ] Partiel | |
| [Framework principal] | [ ] Oui [ ] Non [ ] Partiel | |

**Proof of concept possible en :** [ ] 1 jour  [ ] 1 semaine  [ ] 1 sprint  [ ] > 1 sprint

---

### 5. Risques & Points de vigilance

| Risque | Probabilité (H/M/F) | Impact (H/M/F) | Mitigation |
|---|---|---|---|
| Vendor lock-in | | | |
| Abandon du projet | | | |
| Performance insuffisante | | | |
| Sécurité / CVE connus | | | |
| Courbe d'apprentissage | | | |
| Licencing / coûts cachés | | | |
| [Risque spécifique] | | | |

**Dépendances critiques :**
> [Lister les dépendances lourdes ou risquées]

**CVE / incidents sécurité connus :**
> [Vérifier sur https://nvd.nist.gov/ + GitHub Security Advisories]

---

### 6. Coût d'Adoption

#### 6.1 Effort d'apprentissage

| Profil | Temps estimé pour être opérationnel |
|---|---|
| Dev junior | |
| Dev senior | |
| Toute l'équipe (formation) | |

**Ressources d'apprentissage disponibles :**
> - [ ] Documentation officielle de qualité
> - [ ] Tutoriels vidéo (YouTube / Udemy / Pluralsight)
> - [ ] Cours certifiants
> - [ ] Livre(s) de référence : [titres]
> - [ ] Slack / Discord communautaire actif

#### 6.2 Coût d'intégration

| Dimension | Estimation | Détails |
|---|---|---|
| Migration depuis l'existant | [j/h] | |
| Refactoring nécessaire | [j/h] | |
| Outillage / CI adaptation | [j/h] | |
| Formation de l'équipe | [j/h] | |
| **Total estimé** | **[j/h]** | |

#### 6.3 Coût récurrent (si applicable)

> [Licences, infrastructure, support payant, etc.]
> Prix estimé : ___/mois pour notre usage

---

### 7. Expérimentation

**A-t-on fait un POC ?**
> [ ] Non — à planifier
> [ ] En cours — [qui ? depuis quand ?]
> [ ] Oui — [résultats en 3 lignes]

**Résultats du POC (si fait) :**
> [Ce qui a bien fonctionné / ce qui a bloqué / conclusions]

**Lien vers le repo POC :** [URL ou "N/A"]

---

### 8. Verdict & Recommandation

#### Synthèse des scores

| Dimension | Score | Pondération | Score pondéré |
|---|---|---|---|
| Maturité technique | /25 | x0.25 | /6.25 |
| Communauté | /5 (qualitatif) | x0.20 | /1 |
| Applicabilité | /5 (qualitatif) | x0.30 | /1.5 |
| Risques (inversé) | /5 (qualitatif) | x0.15 | /0.75 |
| Coût d'adoption | /5 (qualitatif) | x0.10 | /0.5 |
| **Total** | | | **/10** |

> **Score de 0 à 3** → Hold
> **Score de 4 à 5** → Assess
> **Score de 6 à 7** → Trial
> **Score de 8 à 10** → Adopt

#### Recommandation finale

**Placement proposé dans le radar :** [ ] Adopt  [ ] Trial  [ ] Assess  [ ] Hold

**Justification en 3 lignes :**
>

**Prochaine action recommandée :**
> [ ] Faire un POC de ___ jours sur le use case [X]
> [ ] Remplacer [technologie actuelle] par celle-ci dans [contexte]
> [ ] Surveiller pendant 2 trimestres avant réévaluation
> [ ] Ne pas adopter car [raison]
> [ ] Former l'équipe et passer en production sur [projet]

**À réévaluer le :** [YYYY-MM-DD ou "au prochain trimestre"]

---

### 9. Références

| Type | Lien | Note |
|---|---|---|
| Site officiel | | |
| GitHub | | |
| Documentation | | |
| Article de référence | | |
| Benchmark | | |
| Talk / conférence | | |

---

### 10. Historique des évaluations

| Date | Évaluateur | Statut radar | Changement |
|---|---|---|---|
| [date] | [nom] | [statut] | Première évaluation |
| | | | |

---

*Fiche générée selon le template v1.0 — Programme de Veille Technologique*
```

---

## Exemple rempli : Bun (runtime JavaScript)

```
# Bun — Fiche d'Évaluation

**Domaine :** Frontend & Expérience Dev
**Auteur :** Marie Dupont
**Date d'évaluation :** 2025-09-15
**Version évaluée :** 1.1.20
**Statut radar proposé :** [x] Trial
```

### 1. Présentation

**En une phrase :**
> Bun est un runtime JavaScript tout-en-un (exécution, bundler, test runner, package manager) écrit en Zig, conçu pour être drastiquement plus rapide que Node.js.

**Problème résolu :**
> Nos builds frontend prennent 4 min en CI. Le npm install seul = 45 sec. Bun promet 10-30x de gain.

**Alternatives connues :**
> - Node.js 22 — standard de facto, écosystème maximal
> - Deno 2 — sécurité first, compatible Node, moins rapide que Bun

### 2. Maturité Technique

| Critère | Score | Justification |
|---|---|---|
| Stabilité de l'API | 4/5 | Stable depuis v1.0 (sept 2023), quelques edge cases |
| Documentation | 5/5 | Excellente, claire, exemples concrets |
| Tests de la lib | 4/5 | Suite de tests solide |
| Fréquence releases | 5/5 | Releases hebdomadaires |
| Breaking changes | 4/5 | Semver respecté depuis v1.0 |
| **Score maturité** | **22/25** | |

### 8. Verdict

**Placement proposé :** Trial

**Justification :** Maturité suffisante (v1.1), communauté active (72k étoiles), gains de performance mesurés sur notre CI (POC : -65% sur le build). Risque principal = compatibilité native Node (addons C++). Notre stack React/TypeScript sans addons natifs est compatible à 98%.

**Prochaine action :** Migrer le pipeline CI d'un projet pilote (frontend-dashboard) sur 1 sprint. Mesurer gains réels.

---

## Conseils de remplissage

- **Section 1 obligatoire** : si on ne sait pas expliquer en une phrase, l'évaluation est prématurée
- **Section 3** : utiliser [star-history.com](https://star-history.com/) pour visualiser la trajectoire GitHub
- **Section 6** : être honnête sur les coûts — sous-estimer est le biais le plus commun
- **Section 8** : le score est un outil de discussion, pas un oracle — le verdict peut diverger du score si le contexte le justifie (noter pourquoi)
