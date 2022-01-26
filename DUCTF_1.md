#How to pronounce GIF

**1. Telecharger le fichier "challenge.gif".**
Une fois que le fichier est téléchargé on obtien un gif composé de plusieur *frame* de QR codes.
**2. Décomposition le gif.**
On va convertir le gif en plusieurs image format png (toutes les images qui composent le gif)
'''bash
convert challenge.gif %04d.png 
'''

**3. Recomposion des QR codes.**
