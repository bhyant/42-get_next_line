# get_next_line - Projet 42

## 📚 Description

**get_next_line** est un projet du cursus 42 qui consiste à écrire une fonction capable de lire, de manière efficace, une ligne à la fois depuis un descripteur de fichier. La fonction doit retourner chaque ligne lue, y compris le retour à la ligne, et fonctionner pour n'importe quel type de fichier ou d'entrée standard.

Ce projet est idéal pour travailler la gestion de la mémoire, la manipulation de buffers, et l’utilisation des appels système tels que `read`.

---

## 🛠️ Fonctionnalités

- Lecture ligne par ligne depuis un ou plusieurs fichiers (ou stdin)
- Gestion efficace du buffer
- Prise en charge de plusieurs descripteurs de fichiers simultanément
- Retourne chaque ligne, avec ou sans saut de ligne
- Respect du prototype imposé :  
  ```c
  char *get_next_line(int fd);
  ```

---

## 📂 Structure du projet

- `get_next_line.c` : Fonction principale et logique de lecture
- `get_next_line_utils.c` : Fonctions utilitaires (gestion de chaînes, mémoire…)
- `get_next_line.h` : Header avec le prototype et les définitions
- `Makefile` : Compilation du projet

---

## 🚀 Utilisation

### 1. Compilation

```bash
make
```

### 2. Utilisation dans vos projets

Incluez le header dans votre code :

```c
#include "get_next_line.h"
```

Exemple d’utilisation :

```c
int fd = open("fichier.txt", O_RDONLY);
char *line;
while ((line = get_next_line(fd)) != NULL)
{
    printf("%s", line);
    free(line);
}
close(fd);
```

---

## 📝 Contraintes

- Respect du prototype demandé
- Gestion correcte de la mémoire (aucune fuite)
- Fonctionne avec plusieurs descripteurs en parallèle
- Interdiction d’utiliser des fonctions de la libc non autorisées

---

## 💡 Conseils

- Testez avec des fichiers de tailles et contenus variés
- Vérifiez les comportements en fin de fichier et avec des fichiers vides
- Utilisez `valgrind` pour traquer les fuites de mémoire
- Respectez la norme de codage 42 (Norminette)

---

## 👤 Auteur

Projet réalisé par [bhyant](https://github.com/bhyant) dans le cadre du cursus 42.
