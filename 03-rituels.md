# Rituels de Partage Technologique

> Objectif : transformer la veille individuelle en connaissance collective, sans surcharger les agendas.
> Budget temps total : **~2h/semaine/développeur** (veille + rituels combinés).

---

## Vue d'ensemble du calendrier

```
SEMAINE TYPE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Lun  Mar  Mer  Jeu  Ven
                          ← 1h veille individuelle (async)
          [Tech Talk]          ← 30 min tous les 15 jours
                    [Brown Bag] ← 1h mensuel (vendredi midi)

TRIMESTRE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Mois 1  →  Mois 2  →  Mois 3  →  [Hack Day + Radar Update]
```

---

## Rituel 1 — Tech Talk bi-hebdomadaire

**Fréquence :** Toutes les 2 semaines (mercredi 10h00–10h30)
**Durée :** 30 minutes fixes
**Format :** 1 ou 2 présentations de 10-15 min chacune
**Lieu :** Salle de réunion principale / call vidéo

### Structure d'une session

```
00:00 – 02:00  Intro & contexte (animateur)
02:00 – 15:00  Présentation #1 (technologie ou article)
15:00 – 20:00  Questions / discussion
20:00 – 28:00  Présentation #2 (optionnelle si temps le permet)
28:00 – 30:00  Décision : fiche d'évaluation à ouvrir ? vote radar ?
```

### Règles du Tech Talk

- **Pas de slides obligatoires** — une démo, un article partagé à l'écran, ou une fiche d'évaluation suffisent
- **Le présentateur n'est pas un expert** — il partage ce qu'il a trouvé intéressant, pas ce qu'il maîtrise
- **Questions courtes** — les débats longs sont déplacés en canal async
- **Un sujet = une décision** : à la fin, l'équipe dit "on ouvre une fiche", "on met en Watch", ou "on passe"
- Rotation des présentateurs : chacun présente ~1 fois par mois (backlog de sujets dans le canal #veille)

### Backlog de sujets

Maintenu dans le canal Slack/Teams `#veille-tech` avec le format :
```
[SUJET] Nom de la techno / article — proposé par @nom — domaine: IA/Cloud/etc
```

---

## Rituel 2 — Brown Bag Lunch mensuel

**Fréquence :** 1er vendredi du mois, 12h00–13h00
**Durée :** 1 heure
**Format :** Présentation approfondie + démo + débat
**Lieu :** Salle de conf + sandwich/pizza pris en commun
**Audience :** Toute l'équipe tech, ouvert aux non-techs (PM, design)

### Sujets privilégiés

- Technologies en phase **Trial** ou **Assess** sur le radar
- Retours d'expérience sur une adoption récente
- Comparatif de 2-3 alternatives (ex: "Kafka vs Pulsar vs NATS")
- Présentation d'un livre ou d'une conférence majeure (résumé)
- Invitation d'un speaker externe (communauté locale, conférencier)

### Structure

```
00:00 – 05:00  Contexte : pourquoi ce sujet maintenant ?
05:00 – 35:00  Présentation principale + démo live si possible
35:00 – 50:00  Discussion ouverte : avantages / risques / applicabilité chez nous
50:00 – 60:00  Vote : placement dans le radar ? next steps ?
```

### Vote de placement radar

À la fin du Brown Bag, si la technologie est suffisamment mature pour décision :

```
Sondage rapide (outil : Mentimeter / Slido / poll Slack)

"Où placeriez-vous [technologie] dans notre radar ?"
  ○ Adopt   — prêt à utiliser en production maintenant
  ○ Trial   — faire un POC sur un vrai projet sous 1 trimestre
  ○ Assess  — continuer la veille, pas encore d'action
  ○ Hold    — ne pas adopter / retirer de la stack

Règle de décision : majorité simple, discussion si résultat partagé 50/50
```

---

## Rituel 3 — Hack Day trimestriel

**Fréquence :** 1 jour par trimestre (dernier vendredi du mois 3)
**Durée :** 1 journée complète (9h00–18h00)
**Format :** Exploration libre + démo finale
**Objectif :** Tester des technologies en zone "Trial" ou "Assess" du radar

### Déroulement

```
09:00 – 09:30  Kickoff : présentation des défis & équipes
09:30 – 12:30  Sprint 1 — exploration / setup / premier prototype
12:30 – 13:30  Déjeuner commun
13:30 – 16:30  Sprint 2 — développement / tests
16:30 – 17:30  Démos (5 min / équipe, format "show don't tell")
17:30 – 18:00  Rétrospective + mise à jour du radar
```

### Règles du Hack Day

- **Équipes de 2-3 personnes** — cross-fonctionnelles si possible
- **Sujet imposé** : 1 technologie du radar en zone Trial ou Assess (tiré au sort ou voté)
- **Sujet libre** : les 30% restants peuvent explorer ce qu'ils veulent
- **Livrable minimum** : un repo avec README + 5 min de démo
- Pas de jugement sur la qualité — c'est une exploration, pas un projet

### Critères d'évaluation post-Hack Day

Après la journée, chaque équipe remplit en 10 min :

| Question | Réponse |
|---|---|
| La techno tient ses promesses ? | Oui / Non / Partiellement |
| Facilité d'adoption (1-5) | |
| Surprise positive ? | |
| Surprise négative / blocage ? | |
| On recommande Trial → Adopt ? | Oui / Non / Pas encore |

---

## Rituel 4 — Mise à jour trimestrielle du Radar

**Fréquence :** 1 fois par trimestre (semaine suivant le Hack Day)
**Durée :** 2 heures
**Participants :** Tech leads + contributeurs principaux de fiches

### Processus de mise à jour

**Semaine -2 : Collecte**
- Chaque développeur propose 1-3 technologies à réviser dans le canal `#veille-tech`
- Les fiches d'évaluation des nouvelles technologies sont finalisées
- Un "radar owner" (rôle tournant chaque trimestre) collecte les propositions

**Semaine -1 : Pré-vote async**
- Le radar owner envoie la liste des technologies à voter
- Chaque membre de l'équipe vote en async (formulaire Google / Notion / Miro)
- Durée : 30 min max pour voter

**Jour J : Session de mise à jour (2h)**

```
00:00 – 20:00  Review des technologies consensuelles (votes unanimes)
               → Direct placement sans débat
20:00 – 80:00  Débat sur les technologies controversées (votes partagés)
               → Règle : 10 min max par techno
80:00 – 100:00 Validation du radar final
100:00 – 120:00 Publication + communication à l'équipe élargie
```

**Après la session**
- Mise à jour du fichier `04-tech-radar.md`
- Publication dans le canal `#engineering-all`
- Archivage de la version précédente dans `archives/radar-YYYY-QX.md`

---

## Budget temps récapitulatif

| Rituel | Fréquence | Durée | Temps/mois |
|---|---|---|---|
| Veille individuelle | Hebdomadaire | 1h | 4h |
| Tech Talk | Bi-hebdomadaire | 30 min | 1h |
| Brown Bag Lunch | Mensuel | 1h | 1h |
| Hack Day | Trimestriel | 8h | 2.7h |
| Mise à jour radar | Trimestriel | 2h | 0.7h |
| **Total mensuel** | | | **~9.4h** |
| **Total hebdomadaire** | | | **~2.3h** |

> Légèrement au-dessus de 2h/semaine en comptant le Hack Day.
> Hors Hack Day : **~1.7h/semaine** — bien dans l'enveloppe.
> Le Hack Day peut être ajusté à une demi-journée si contrainte forte.

---

## Outils recommandés

| Usage | Outil | Alternatif |
|---|---|---|
| Backlog de sujets | Canal Slack `#veille-tech` | Notion board |
| Fiches d'évaluation | Fichiers Markdown dans ce repo | Notion template |
| Votes radar | Google Forms / Mentimeter | Poll Slack |
| Radar visuel | [radar.thoughtworks.com](https://radar.thoughtworks.com) (custom) | Miro |
| Enregistrement des talks | Loom / Zoom (si remote) | N/A |
| Newsletter interne | Notion page mensuelle | Email digest |
