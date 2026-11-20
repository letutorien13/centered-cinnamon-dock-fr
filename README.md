# Traduction française — Centered Cinnamon Dock

Traduction française de l’extension Cinnamon [Centered Cinnamon Dock](https://github.com/linuxmint/cinnamon-spices-extensions/tree/master/centered-cinnamon-dock@mostlynick3) (`centered-cinnamon-dock@mostlynick3`, auteur mostlynick3, Cinnamon 6.4).

L’extension transforme un panneau en dock flottant centré : coins arrondis, ombre, transparence, largeur minimale, décalage vertical, zoom au survol et masquage automatique. Les réglages s’ouvrent par un clic droit sur le panneau.

## Fichier

`po/fr.po` traduit les 39 chaînes de l’interface :

- le dialogue de bienvenue ;
- les paramètres du dock (général, apparence, masquage automatique, indicateur, couleur) ;
- le nom et la description de l’extension.

Le français suit le vocabulaire de Cinnamon : panneau, moniteur, Activer, Annuler, Appliquer. Le nom affiché est **Dock Cinnamon centré**.

## Installation

L’extension doit déjà être installée, et la session en français. Elle charge les traductions depuis `~/.local/share/locale`.

```bash
mkdir -p ~/.local/share/locale/fr/LC_MESSAGES
msgfmt -c -o ~/.local/share/locale/fr/LC_MESSAGES/centered-cinnamon-dock@mostlynick3.mo po/fr.po
cp po/fr.po ~/.local/share/cinnamon/extensions/centered-cinnamon-dock@mostlynick3/po/fr.po
```

Puis redémarrez Cinnamon : Alt+F2, tapez `r`, validez.

`msgfmt` vient du paquet `gettext`.

## Limite

Dans le dialogue de bienvenue, la liste des panneaux est écrite en dur dans `extension.js` (`bottom (Monitor 0)`, etc.). Ces libellés ne passent pas par gettext : le titre et les boutons sont traduits, la liste reste en anglais.
