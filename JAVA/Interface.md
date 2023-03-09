# Interface

En Java, une interface est une structure qui définit un ensemble de méthodes abstraites (sans implémentation concrète) qui doivent être implémentées par une classe qui implémente l'interface. Une interface peut également inclure des constantes et des méthodes par défaut (implémentées avec une implémentation par défaut).

Les interfaces sont définies à l'aide du mot clé "interface" suivi du nom de l'interface et des méthodes et des constantes qu'elle contient. Voici un exemple simple :

```
public interface MonInterface {
public void methode1();
public int methode2(String parametre);
public static final int MA_CONSTANTE = 42;
}
```
Dans cet exemple, l'interface "MonInterface" définit deux méthodes abstraites : "methode1" qui ne prend aucun argument et ne renvoie rien, et "methode2" qui prend une chaîne de caractères en argument et renvoie un entier. L'interface définit également une constante "MA_CONSTANTE" qui a une valeur de 42.

Une classe peut implémenter une interface en utilisant le mot clé "implements". Voici un exemple :

```
public class MaClasse implements MonInterface {
public void methode1() {
// Implémentation de la méthode 1
}

public int methode2(String parametre) {
// Implémentation de la méthode 2
return 0;
}
}
```
Dans cet exemple, la classe "MaClasse" implémente l'interface "MonInterface" en fournissant une implémentation pour les méthodes abstraites "methode1" et "methode2". La classe doit implémenter toutes les méthodes abstraites définies dans l'interface.

Les interfaces sont souvent utilisées pour créer des contrats entre différentes parties d'un programme. Par exemple, une interface peut définir les méthodes qu'un plugin doit implémenter pour fonctionner avec une application. Les interfaces permettent également de créer des classes qui implémentent des comportements différents pour une même méthode. Cela peut être utile pour créer des algorithmes génériques qui peuvent être utilisés avec différents types de données.


# Collection

En Java, les collections sont des structures de données qui permettent de stocker et de manipuler des groupes d'objets. Elles sont fournies par la bibliothèque standard de Java et sont disponibles pour une utilisation immédiate dans tous les programmes Java.

Les collections Java sont organisées dans une hiérarchie de classes et d'interfaces. La classe de base est "java.util.Collection", qui définit les méthodes de base que toutes les collections doivent avoir, telles que "add", "remove" et "size". Les interfaces telles que "java.util.List", "java.util.Set" et "java.util.Map" étendent "Collection" et ajoutent des méthodes supplémentaires pour des types de collections spécifiques.

Voici un aperçu des principales collections Java :

- List : une liste ordonnée d'éléments qui permet l'accès par indice, tel que "ArrayList" ou "LinkedList".
- Set : une collection d'éléments distincts qui ne permet pas de doublons, tel que "HashSet" ou "TreeSet".
- Map : une association d'éléments clés/valeurs, où chaque élément est accessible par une clé unique, tel que "HashMap" ou "TreeMap".
- Queue : une collection d'éléments qui suit le principe "premier entré, premier sorti" ou "premier entré, dernier sorti", tel que "PriorityQueue" ou "ArrayDeque".
- Stack : une collection d'éléments qui suit le principe "dernier entré, premier sorti", tel que "Stack" ou "LinkedList".

Les collections Java offrent de nombreuses fonctionnalités et méthodes pratiques pour manipuler les éléments, telles que l'ajout, la suppression, la recherche, la tri, la conversion, le filtrage, l'itération et bien plus encore. Les collections sont également optimisées pour les performances et la gestion de la mémoire, ce qui les rend efficaces pour une utilisation dans de nombreux types de programmes.


En résumé, les collections Java sont des structures de données flexibles et puissantes qui facilitent la manipulation de groupes d'objets. Elles offrent de nombreuses fonctionnalités pratiques et sont optimisées pour les performances et la gestion de la mémoire.

Voici quelques exemples de code pour différentes collections en Java:

- ArrayList - une implémentation de la collection List

```
import java.util.ArrayList;

public class ExampleArrayList {
public static void main(String[] args) {
ArrayList<String> fruits = new ArrayList<String>();
fruits.add("pomme");
fruits.add("banane");
fruits.add("orange");

        System.out.println(fruits.get(0)); // affiche "pomme"

        fruits.remove("banane");

        System.out.println(fruits.size()); // affiche 2
    }
}
```
- HashSet - une implémentation de la collection Set
```
import java.util.HashSet;

public class ExampleHashSet {
public static void main(String[] args) {
HashSet<String> fruits = new HashSet<String>();
fruits.add("pomme");
fruits.add("banane");
fruits.add("orange");

        System.out.println(fruits.contains("banane")); // affiche true

        fruits.remove("banane");

        System.out.println(fruits.size()); // affiche 2
    }
}
```

- HashMap - une implémentation de la collection Map

```
import java.util.HashMap;

public class ExampleHashMap {
public static void main(String[] args) {
HashMap<String, Integer> fruits = new HashMap<String, Integer>();
fruits.put("pomme", 1);
fruits.put("banane", 2);
fruits.put("orange", 3);

        System.out.println(fruits.get("banane")); // affiche 2

        fruits.remove("banane");

        System.out.println(fruits.size()); // affiche 2
    }
}
```
Ces exemples ne sont que la pointe de l'iceberg en termes de ce que vous pouvez faire avec les collections en Java. J'espère que cela vous donne une idée de base de ce que sont les collections en Java et de la manière dont elles peuvent être utilisées.

# Liste 

En Java, une liste est une collection d'éléments ordonnés qui peut être parcourue séquentiellement. Il existe plusieurs types de listes en Java, mais la plus courante est l'interface List, qui peut être implémentée par plusieurs classes, notamment ArrayList et LinkedList. Voici un exemple de code utilisant ArrayList:

```
import java.util.ArrayList;

public class ListeExemple {
public static void main(String[] args) {

      // Créer une liste vide
      ArrayList<String> liste = new ArrayList<String>();

      // Ajouter des éléments à la liste
      liste.add("Premier élément");
      liste.add("Deuxième élément");
      liste.add("Troisième élément");

      // Accéder à un élément de la liste
      System.out.println("Le deuxième élément est : " + liste.get(1));

      // Modifier un élément de la liste
      liste.set(0, "Nouveau premier élément");

      // Supprimer un élément de la liste
      liste.remove(2);

      // Parcourir la liste avec une boucle for-each
      for (String element : liste) {
         System.out.println(element);
      }
}
}
```
Dans cet exemple, nous créons une liste vide en utilisant la classe ArrayList. Ensuite, nous ajoutons quelques éléments à la liste en utilisant la méthode add(). Nous accédons à un élément spécifique de la liste en utilisant la méthode get(). Nous modifions un élément de la liste en utilisant la méthode set(). Nous supprimons un élément de la liste en utilisant la méthode remove(). Enfin, nous parcourons la liste à l'aide d'une boucle for-each
