# reflex

REFLEX — deux mini-jeux de réflexes qui utilisent la webcam, dans une seule page
HTML sans build ni dépendance à installer.

- **🔴 Cercle Rouge** — un cercle rouge apparaît directement sur toi. Au moment
  exact où le compte à rebours atteint zéro, un scan vérifie si une partie de ton
  corps est encore dedans. À partir de la manche 6, le cercle bouge et de petits
  cercles supplémentaires apparaissent. Ce mode ne se met jamais en pause.
- **🔵 Cercle Bleu** — un cercle bleu apparaît loin de toi : touche-le avec
  n'importe quelle partie de ton corps avant la fin du temps. Il rétrécit à
  chaque manche et se met en pause si tout ton corps n'est plus visible.

Dix manches par jeu, difficulté croissante.

## Lancer le jeu

L'accès à la webcam exige une origine sécurisée : ouvre la page via `https://`
ou `localhost` (un simple `file://` ne suffit pas).

```sh
python3 -m http.server 8000
# puis http://localhost:8000/index.html
```

## Vie privée

Le suivi de pose tourne entièrement dans le navigateur via
[MediaPipe Tasks Vision](https://ai.google.dev/edge/mediapipe). Aucune image ni
vidéo n'est envoyée, enregistrée ou partagée. Une connexion internet est
nécessaire au premier lancement pour télécharger le modèle et le runtime WASM
depuis le CDN.
