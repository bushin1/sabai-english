# Sabai English v3 — spec (2026-10-11)

Objectif : Marvin (A2, Thaïlande) veut PARLER en anglais au quotidien : expliquer ce qu'il veut (coiffeur), raconter sa journée, parler de ce qu'il aime. Il veut des méthodes prouvées et voir ses progrès.

## Principes (recherche)
- Output + feedback correctif (Swain ; méta-analyses Li 2010, Lyster & Saito 2010) : il parle, Claude corrige et extrait les mots manquants.
- Rappel actif (Roediger & Karpicke 2006) : FR → il dit en anglais → vérifie. Plus de QCM.
- Répétition espacée (Cepeda 2006) de SES trous : boîtes J+0/1/3/7/14/30.
- Vocabulaire fréquent (Nation 2006) : banque de 292 mots, en rappel actif.
- Shadowing (Hamada 2016) : répéter la version corrigée, lent puis normal.
- Progrès visible : liste « je peux déjà » (can-do CECRL), erreurs/100 mots, mots actifs, niveau estimé, bilan hebdo.

## Boucle quotidienne (15 min)
1. Parler : consigne FR du jour (liée à un objectif can-do) → il dicte en anglais (micro clavier) → Claude : version corrigée, 3 manques, conseil, erreurs/100 mots, consigne réussie ?
2. Répéter la version corrigée (TTS lent/normal).
3. Rappel : mots dus, FR → EN, auto-évaluation.
4. Écouter : situation du jour (exercices v2 conservés).
5. Mesure : placement initial (2 min de parole libre) ; bilan hebdo sur sujet fixe ; graphe erreurs/100 mots.

## Onglets
Parler (accueil) · Écouter · Mots (mes mots + banque) · Progrès.

## DA : piste « Nuit »
Graphite #0F1012, cartes #17181B, ambre #F0B35B, vert #5CC08C, Sora + JetBrains Mono. Thème clair fourni. Pas d'XP, de confettis ni de sons : série et mesures seulement.

## Données
state v3 : settings, streak, days{date:{parle,listen}}, words, hard, listen (session écoute), parle (session du jour), level, baseline, measures[], cando{}, seen{}. Migration depuis v2. Sauvegarde localStorage + db `progress/main` (artifact).

## Hébergement
Primaire : artifact claude.ai (capacités sample + db). Miroir public GitHub Pages sans correction Claude.
