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

## Ajout v3.1 (2026-10-12) : QCM rapides
- Écouter → « Dialogue du jour » : 12 dialogues à deux voix (TTS, deux voix si dispo), écoute sans texte, 3 QCM en français (sujet, détail chiffré, réplique clé), puis texte + réécoute. Séquence écouter → vérifier → lire → réécouter (approche métacognitive, Vandergrift).
- Mots → « Quiz éclair » : 10 QCM, 4 choix, moitié EN→FR moitié FR→EN, mélange de ses mots et de la banque ; un raté sur un mot perso remet sa boîte à 1, un raté sur la banque l'ajoute à ses mots.

## Ajout v3.2 (2026-10-16) : anglais pro
- Banque pro : 4 thèmes (SEO, SEO local et fiche Google, Claude Code et dev, parler à un client), ~80 termes avec exemple en contexte, rappel actif et quiz comme le reste.
- 3 dialogues pro (fiche suspendue, script planté, chute de positions) + bouton « Dialogue pro ».
- Objectif can-do « Expliquer mon métier » : 6 consignes de parole, bouton « Plutôt une consigne pro ».
- « Depuis un texte » : coller un texte anglais lu au travail, Claude extrait 6 termes utiles (sens + exemple), à garder dans ses mots. Principe : vocabulaire issu de l'input authentique dont il a besoin, puis répétition espacée et réemploi en production.

## Ajout v3.3 (2026-10-17) : QCM conversation et QCM pro
- QCM conversation : 40 situations (salle de sport, mon métier, rencontres, relancer, rattraper). On entend la phrase de l'autre, on choisit la réplique naturelle parmi 4 (les pièges sont du franglais ou des réponses sèches), puis traduction, pourquoi, réécoute, à dire à voix haute. Les ratés deviennent des « mots » à réviser. Principe : blocs préfabriqués (formulaic sequences) qui donnent la fluidité à l'oral.
- QCM vocabulaire pro : même quiz que « Mélange » mais limité à la banque pro et aux mots issus de textes.
- Accès direct depuis l'accueil Parler.
