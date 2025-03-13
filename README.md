# witcher1_save_editor
Tool to modify the witcher 1 (enhanced edition) save files (modified functional version). You will be able to modify your items, your mutagens and the characteristics of your character.

TWEditor - Version 2.2

Fichier original : Ronald Hoffman
Présentation

TWEditor vous permet de modifier les fichiers de sauvegarde créés par The Witcher. Vous pouvez ajuster les attributs et les compétences du personnage principal, Geralt. Vous avez également la possibilité de décompresser tous les fichiers de la sauvegarde, de modifier manuellement un ou plusieurs fichiers, puis de recompresser la sauvegarde. Il est important de noter qu'il n'est pas possible d'ajouter ou de supprimer des fichiers dans la sauvegarde.

L'onglet 'Stats' vous permet de modifier certains champs de la sauvegarde, tels que l'expérience, les orens et les talents. Les valeurs modifiées seront enregistrées lors de l'enregistrement du fichier. L'acceptation de ces changements lors du chargement de la sauvegarde dépend du moteur du jeu.

L'onglet 'Attributes' permet de modifier les sélections de Force, Dextérité, Endurance et Intelligence.

L'onglet 'Signs' permet de modifier les sélections de Aard, Igni, Quen, Axii et Yrden.

L'onglet 'Styles' permet de modifier les sélections pour l'épée en acier et l'épée en argent.

L'onglet 'Equipment' vous permet de modifier les objets équipés par Geralt ainsi que ses trophées.

L'onglet 'Inventory' permet de modifier l'inventaire de Geralt.

L'onglet 'Quests' affiche les quêtes du jeu (en cours, terminées, échouées et non commencées). Le bouton 'Examine' permet d'afficher la description de l'étape actuelle de la quête (si une description est disponible pour cette étape).
Installation

Cette version de l'éditeur de sauvegarde nécessite l'édition améliorée de The Witcher. L'utilisation de cette version de l'éditeur avec la version originale de The Witcher pourrait entraîner des erreurs d'inventaire.

Pour installer cet utilitaire, placez le fichier TWEditor.jar dans un répertoire de votre choix. Pour exécuter l'utilitaire, créez un raccourci et spécifiez la commande suivante :

javaw -Xmx256m -jar TWEditor.jar

Comme programme à exécuter. Définissez le répertoire de démarrage sur le répertoire où vous avez extrait le fichier jar. Un raccourci de programme est fourni à titre d'exemple. L'argument -Xmx256m spécifie la taille maximale du tas en mégaoctets (dans cet exemple, 256 Mo). Vous pouvez augmenter la taille si vous rencontrez des problèmes de mémoire lors du traitement de grandes sauvegardes. Notez que Windows commencera à échanger si la taille du tas Java dépasse l'espace de stockage disponible, ce qui affectera considérablement les performances. La machine virtuelle Java échouera à démarrer si la taille du tas demandée est trop grande.

L'exécution de l'éditeur nécessite la version 1.6 de Java (JRE 1.6). Vous pouvez télécharger la version nécessaire depuis Java.com. Si vous n'êtes pas sûr de la version de Java installée sur votre système, ouvrez une fenêtre de commande et tapez "java -version".

Le répertoire d'installation du jeu est localisé en scannant le registre Windows. Si cette opération échoue ou si les fichiers du jeu se trouvent dans un autre répertoire, vous pouvez spécifier le répertoire d'installation du jeu lors du lancement de l'éditeur en ajoutant l'option suivante à la ligne de commande Java : -DTW.install.path="<chemin>" où <chemin> est le répertoire contenant dialog.tlk. Par exemple, si les fichiers du jeu sont installés dans C:\Games\The Witcher et l'éditeur dans C:\Games, le raccourci ressemblera à ceci :

javaw -DTW.install.path="C:\Games\The Witcher" -jar TWEditor.jar

N'oubliez pas de mettre des guillemets autour du chemin.

L'identifiant de langue est déterminé par une analyse du registre Windows. Si cette analyse échoue ou si vous souhaitez utiliser une autre langue, vous pouvez spécifier l'identifiant de langue en ajoutant l'option -DTW.language=n où n correspond à l'identifiant de langue pour le fichier .tlk correspondant. Par exemple, pour l'anglais américain, utilisez :

javaw -DTW.language=3 -jar TWEditor.jar

Le répertoire des données du jeu est supposé être "The Witcher" dans le dossier des documents de l'utilisateur (dossier "Mes Documents" sur un système en anglais). Si les sauvegardes sont situées dans un autre répertoire, vous pouvez spécifier le répertoire de données du jeu en ajoutant l'option suivante à la ligne de commande Java : -DTW.data.path="<chemin>" où <chemin> est le répertoire contenant les données du jeu. Par exemple, si l'utilisateur s'appelle Ronald Hoffman, le répertoire normal des données serait :

C:\Documents and Settings\Ronald Hoffman\My Documents\The Witcher

Il arrive que le runtime Java génère une exception de type "null pointer" lorsqu'il ajoute les dossiers du shell au dialogue du sélecteur de fichiers (JFileChooser). Si cela se produit, vous pouvez désactiver les dossiers du shell en ajoutant l'option -DUseShellFolder=0 à la ligne de commande Java.
=========================================================================

Version 1.0 :
Lancement initial.

Version 1.1 :
Ajout du support de l'inventaire (ajouter/supprimer/examiner).

Version 1.2 :
Un flux d'entrée ouvert provoquait l'échec intermittent de la sauvegarde.
Le mnémonique du signe Axii était "Axi" et non "Axii", ce qui causait des erreurs lors de l'édition du signe Axii.

Version 1.3 :
Ouverture des sauvegardes créées sur un système russe.
Ajout de l'onglet 'Quests'.

Version 1.4 :
Utilisation de la taille de pile maximale lors de l'ajout d'un objet à l'inventaire.

Version 1.5 :
Correction d'une exception de pointeur nul lors de la modification d'un signe sans signes appris.

Version 2.0 :
Support de plusieurs langues installées.
Ajout de la possibilité de recompresser un fichier de sauvegarde.
Support du système de gestion d'inventaire élargi de l'édition améliorée.

Version 2.1 :
Support des objets équipés.

Version 2.2 :
Demande du répertoire d'installation du jeu si celui-ci n'est pas trouvé dans le registre Windows ou s'il est invalide.
Demande de l'identifiant de langue si celui-ci n'est pas trouvé dans le registre Windows.
Compatibilité complète avec Windows 10.
