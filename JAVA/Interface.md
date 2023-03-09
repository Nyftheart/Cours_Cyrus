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
