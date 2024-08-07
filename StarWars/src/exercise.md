# StarWars

## Doc Java
https://devdocs.io/openjdk~21/

## Objectif

- Comprendre l'utilité des classes abstraites et des méthodes abstraites.
- Comprendre l'utilité des interfaces.
- Comprendre l'héritage en Java.
- Comprendre l'utilité des différentes collections Java.


## Exercice

### 1. Création du projet

- Créez un package `master`.
- Créez une classe abstraite `Master` dans le package `master`.
- Ajoutez les attributs suivants à la classe `Master` :
  - `name` de type `String`
  - `hp` de type `int`
  - `damage` de type `int`
- Ajoutez un constructeur à la classe `Master` prenant en paramètres `name`, `hp` et `damage`.
- Ajoutez des getters et des setters pour les attributs de la classe `Master`.
- Ajoutez les méthodes suivantes à la classe `Master` :
  - `attack(Master target)`: méthode abstraite pour infliger des dégâts à un autre `Master`.
  - `isAlive()`: renvoie `true` si le `Master` a des points de vie restants, sinon `false`.
  - `toString()`: renvoie une chaîne de caractères contenant le nom et les points de vie du `Master`.

### 2. Création de l'interface `ForceUser`

- Créez une interface `ForceUser` dans le package `master`.
- Définissez la méthode suivante dans l'interface `ForceUser` :
  - `useForce(Master target)`: représente une capacité spéciale utilisant la Force contre un autre `Master`.

### 3. Création des classes `Jedi` et `Sith`

- Créez une classe `Jedi` qui hérite de `Master` et implémente l'interface `ForceUser`.
  - Implémentez les méthodes abstraites `attack` et `defend` dans `Jedi`.
  - Ajoutez un attribut `force` de type `int` à la classe `Jedi`.
  - Implémentez la méthode `useForce` :
    - `forcePush(Master target)`: repousse un `Master` toutes les 5 attaques et inflige autant de dégats qu'il a de force. Bonus : Un `Master` repoussé ne peut pas attaquer pendant 2 tours.

- Créez une classe `Sith` qui hérite de `Master` et implémente l'interface `ForceUser`.
  - Implémentez les méthodes abstraites `attack` et `defend` dans `Sith`.
  - Implémentez la méthode `useForce` :
    - `lighting(Master target)`: inflige 150% des dégâts à un `Master` toutes les 6 attaques.
    - `stroke(Master target)`: inflige 50% des dégâts à un `Master` toutes les 2 attaques.

### 4. Création d'une collection de `Master`

- Créez une `HashMap` de `Master` dans la classe `Main`.
- Ajoutez des `Jedi` et des `Sith` à la collection.
- Faites attaquer les `Jedi` et les `Sith` de la collection.
- Stockez l'historique des attaques dans une `LinkedList`.
