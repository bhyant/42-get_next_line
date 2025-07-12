get_next_line
Description
get_next_line est un projet de l'école 42 qui consiste à créer une fonction capable de lire un fichier ligne par ligne. Ce projet introduit les concepts de lecture par buffer et de gestion de la mémoire statique.
Objectifs
Ce projet permet de :

Maîtriser la lecture de fichiers avec la fonction read
Comprendre la gestion de buffers de taille fixe
Utiliser les variables statiques pour conserver l'état entre les appels
Gérer efficacement la mémoire avec allocation dynamique
Traiter les cas limites (EOF, erreurs, fichiers vides)

Prototype
char *get_next_line(int fd);
Fonctionnement
La fonction lit le fichier associé au descripteur fd et retourne une ligne à chaque appel, incluant le caractère \n s'il existe. Elle retourne NULL quand la fin du fichier est atteinte ou en cas d'erreur.
Paramètres

fd : Descripteur de fichier à lire
BUFFER_SIZE : Taille du buffer de lecture (définie à la compilation)

Partie bonus
La version bonus gère plusieurs descripteurs de fichiers simultanément :

Lecture de plusieurs fichiers en parallèle
Conservation de l'état pour chaque descripteur

Structure du projet
get_next_line/
get_next_line.h
get_next_line.c
get_next_line_utils.c
get_next_line_bonus.h    # Bonus
get_next_line_bonus.c    # Bonus
get_next_line_utils_bonus.c  # Bonus

Contraintes

Utilisation uniquement de read, malloc et free
Pas de variables globales
Gestion de la mémoire sans fuites
Comportement indéfini si le fichier change entre les appels
