# StarWars

## Objectif : 

- Comprendre l'utilité des classes abstraites et des méthodes abstraites.
- Comprendre l'heritage en Java.
- Comprendre l'utilité des différentes collections Java.

---

## Exercice :

1. **Création du projet :**

   - Crée un package 'starwars'.
   - Crée une classe 'Master' dans le package 'starwars'.
   - Ajoute un attribut 'name' de type 'String' à la classe 'Master'.
   - Ajoute un attribut 'hp' de type 'int' à la classe 'Master'.
   - Ajoute un attribut 'def' de type 'int' à la classe 'Master'.
   - Ajoute un attribut 'damage' de type 'int' à la classe 'Master'.
   - Ajoute un constructeur à la classe 'Master' qui prend en paramètre un 'name', un 'hp', un 'def'' et un 'damage'.
   - Ajoute une méthode 'attack' à la classe 'Master' qui prend en paramètre un 'Master' et qui inflige des dégats à ce 'Master'.
   - Ajoute une méthode 'defend' à la classe 'Master' qui prend en paramètre un 'Master' et qui réduit les dégats infligés à ce 'Master'.
   - Ajoute une méthode 'isAlive' à la classe 'Master' qui renvoie 'true' si le 'Master' a des points de vie et 'false' sinon.
   - Ajoute une méthode 'toString' à la classe 'Master' qui renvoie une chaine de caractères contenant le nom et les points de vie du 'Master'.
   - Crée une classe 'Main' qui instancie un 'Master' et qui fait attaquer un autre 'Master'.
   - Affiche le résultat de l'attaque.

2. **Abstaction de la classe 'Master' :**

   - Transforme la classe 'Master' en classe abstraite.
   - Transforme les differentes méthodes en méthode abstraite.

3. **Création des classes 'Jedi' et 'Sith' :**

   - Crée une classe 'Jedi' qui hérite de 'Master'.
   - Crée une classe 'Sith' qui hérite de 'Master'.
   - Implémente les méthodes abstraites de 'Master' dans les classes 'Jedi' et 'Sith'.
   - Rajouter un attribut 'force' de type 'int' à la classe 'Jedi'.
   - Rajouter une méthode 'forcePush' à la classe 'Jedi' qui prend en paramètre un 'Master' et qui repouce ce 'Master' toute les 5 attaques. Un 'Master' repoussé ne peut pas attaquer pendant 2 tours.
   - Rajouter une méthode 'lighting' à la classe 'Sith' qui prend en paramètre un 'Master' et qui inflige 150% des dégats à ce 'Master' toute les 6 attaque.
   - Rajouter une methode 'stroke' à la classe 'Sith' qui prend en paramètre un 'Master' et qui inflige 50% des dégats à ce 'Master' toute les 2 attaque.

4. **Création d'une collection de 'Master' :**

   - Crée une HashMap de 'Master' dans la classe 'Main'.
   - Ajoute des 'Jedi' et des 'Sith' à la collection.
   - Fait attaquer les 'Jedi' et les 'Sith' de la collection.
   - L'historique des attaques sont stockées dans une LinkedList.
