Cassecroute OCR est un outil de scan des fichiers PDF scannés, via [PdfSandwich](http://www.tobias-elze.de/pdfsandwich/), qui offre une interface web basique pour lancer un scan, observer l'avancement, et télécharger le fichier nettoyé.

L'usage principal est le traitement de gros fichiers lourds pour la lecture sur de petits appareils comme des liseuses. Supprimer les images des fichiers PDF (fond, illustrations) et pré-traiter la lecture des caractères permet de largement accélérer le chargement des pages sur une grande variété de modèles de liseuses.

Le traitement de [PdfSandwich](http://www.tobias-elze.de/pdfsandwich/) est simple :

    Lorsqu'un fichier est déposé dans /data/input, il est détecté et le lancement du processus est opéré par autoocr.
    Passage sur le fichier PDF scanné via OCR, afin d'en détecter les éléments textuels et les retranscrire directement textuellement. Ce scan est réalisé grâce au projet Tesseract de reconnaissance de caractères.
    Un fichier PDF sera généré pour chaque page, replaçant le texte approximativement là où il se trouvait dans le document initial. Elles seront ensuite fusionnées.
    La plupart des illustrations disparaissent. Cependant, certains schémas peuvent être conservés après le traitement.
    Vous trouverez le résultat du traitement dans /data/output. Il sera également téléchargeable directement via l'interface.
