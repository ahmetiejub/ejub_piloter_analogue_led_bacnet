
Installation et Configuration
1. Téléchargement
Téléchargez ou clonez ce dépôt dans votre espace de travail ESP-IDF.

Note : Ce projet est spécifiquement conçu pour l'architecture ESP32.

2. Configuration du Wi-Fi
Avant de compiler, vous devez renseigner vos identifiants réseau :

Ouvrez le fichier main/wifi.c.

Modifiez les variables SSID et PASSWORD avec vos informations de connexion.

3. Modification du GPIO (Optionnel)
Par défaut, la sortie est configurée sur le GPIO 23. Pour changer cette broche :

Utilisez le raccourci CTRL + F dans votre éditeur (VS Code ou Espressif IDE).

Recherchez l'occurrence GPIO_NUM_23.

Remplacez-la par votre nouveau numéro de broche dans les deux fichiers suivants :

main/main.c

main/av.c


Une fois la configuration terminée, utilisez les commandes standards ESP-IDF :

Build , Run , et regardé si votre wifi ce connecte a partir du terminal .

Pilotage via YABE
Lancez YABE sur votre PC.

Ajoutez un "Device" en scannant le réseau (IP/UDP).

Une fois l'ESP32 détecté, cherchez l'objet Analog Value.

Modifiez la valeur : comme il s'agit d'une sortie numérique, vous devez modifier le champ "value" et mettre 0 ou 1. Ainsi, vous aurez 3,2 V pour 1 et 0 V pour 0.
