# How to pronounce GIF

## Séparation des images du Gif
**1. Telecharger le fichier "challenge.gif".**

Une fois que le fichier est téléchargé on obtien un gif composé de plusieur *frame* de QR codes.


**2. Décomposition le gif.**

On va convertir le gif en plusieurs image format png (toutes les images qui composent le gif)


```bash
convert challenge.gif %04d.png 
```
## Lecture des QR codes
**3. Recomposion des QR codes.**

On fait une boucle en Bash :
```bash
for i in {0..9}
  do convert -append *${i}.png ${i}out.png
done
```
**4. Lecture des QR codes**
Avec la commande suivante on peut accéder aux informations contenue dans les codes.

```bash
zbarimg *out.png
```
Un retour par codes, dont un rickroll !
Cependant, deux codes retournent une lignes de caratère, on les c/c dans l'ordre (QR code 6 et QR code 8).
Il est possible de le décoder grâce à la commande suivante :
```bash
echo "$encodage" | base64 -d
```
Le Flag est révélé !
