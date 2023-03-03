# Comment fonctionne Java

Java est un langage de programmation orienté objet et une plate-forme informatique qui a été développée par Sun Microsystems (acquise depuis par Oracle Corporation) dans les années 1990. Il est conçu pour être portable, c'est-à-dire qu'il peut être utilisé sur différentes plates-formes matérielles et logicielles, y compris les ordinateurs personnels, les serveurs, les téléphones portables et les tablettes.


Le code source Java est écrit dans des fichiers texte avec une extension de fichier `.java`. Le code est ensuite compilé en bytecode, qui est un code binaire intermédiaire qui peut être exécuté par une machine virtuelle Java (`JVM`). La `JVM` est une couche logicielle qui permet à du code Java d'être exécuté sur différentes plates-formes matérielles sans nécessiter de modification du code source. Cela signifie que le même code Java ***peut être exécuté sur différents systèmes d'exploitation***, tels que Windows, Mac OS et Linux.


Le code Java est organisé en `classes`, qui sont des entités qui contiennent des **données** et des **méthodes**. Les méthodes sont des blocs de code qui effectuent des actions sur les données de la classe. Les classes **peuvent être organisées en paquets**, qui sont des collections de classes liées qui peuvent être facilement réutilisées dans d'autres programmes Java.


Java est souvent **utilisé pour développer des applications de bureau, des applications mobiles, des sites web dynamiques, des jeux vidéo et des applications d'entreprise**. Il dispose d'une vaste bibliothèque standard qui contient des classes pour les entrées/sorties, la gestion des fichiers, les communications réseau, la gestion des données, les interfaces utilisateur, etc. Les développeurs peuvent également créer leurs propres bibliothèques de classes pour des besoins spécifiques.


En résumé, Java est un `langage de programmation portable et `orienté objet` qui utilise une machine virtuelle pour exécuter du code binaire intermédiaire appelé bytecode. Il est largement utilisé pour développer une variété d'applications logicielles et dispose d'une vaste bibliothèque standard pour faciliter le développement.


# La Programmation Orientée Objet (POO)
La `Programmation Orientée Objet (POO)` est un paradigme de programmation qui permet de `structurer les programmes autour d'objets`. Les objets représentent des `entités du monde réel ou des concepts abstraits`. Ils sont des instances de classes qui regroupent des données (appelées propriétés ou attributs) et des comportements (appelés méthodes).

La POO est basée sur quatre concepts fondamentaux :

- ***Encapsulation***: la notion de regrouper des données et des méthodes associées dans une même entité, appelée classe, qui peut être utilisée pour créer des objets. Cela permet de protéger les données de la classe et de ne les rendre accessibles qu'à travers des méthodes publiques.


- ***Héritage*** : permet de créer de nouvelles classes en utilisant les propriétés et les comportements d'une classe existante, appelée classe parent ou superclasse. Les classes filles ou sous-classes héritent des attributs et des méthodes de la classe parent et peuvent les modifier ou en ajouter de nouveaux.


- ***Polymorphisme*** : permet de traiter des objets de différentes classes de manière uniforme en utilisant des méthodes ayant le même nom mais des comportements différents.


- ***Abstraction*** : représente des concepts abstraits de manière concrète en utilisant des classes et des objets.


La POO est largement utilisée dans la `programmation moderne` pour la création d'applications logicielles complexes et de grande envergure. Elle permet de faciliter la maintenance du code, d'améliorer la modularité et la réutilisabilité, et de créer des programmes qui reflètent de manière plus précise les entités du monde réel ou les concepts abstraits.

# Le Garbage Collector

Le Garbage Collector (ou collecteur de déchets) est un `mécanisme de gestion de la mémoire` dans les langages de programmation qui utilisent l'allocation dynamique de mémoire, tels que Java, C# et Python. Le but du garbage collector est de `libérer automatiquement la mémoire` qui n'est plus utilisée par le programme, sans que le programmeur ait à le faire manuellement.

Lorsqu'un programme alloue de la mémoire dynamiquement, il demande à l'ordinateur de lui attribuer un bloc de mémoire pour stocker des données. Le programme peut ensuite utiliser ce bloc de mémoire pour stocker des informations. Lorsque ces informations ne sont plus nécessaires, le programme doit libérer la mémoire en la rendant à l'ordinateur. **Si le programmeur oublie de libérer la mémoire, cela peut entraîner une fuite de mémoire, c'est-à-dire une perte progressive de la mémoire disponible sur le système**.

Le garbage collector `effectue régulièrement des scans de la mémoire utilisée` par le programme pour identifier les objets qui ne sont plus référencés par le programme, c'est-à-dire `les objets qui ne sont plus utilisés ou accessibles`. Il libère ensuite automatiquement la mémoire occupée par ces objets. Le garbage collector peut également déplacer les objets en `mémoire pour optimiser l'utilisation de la mémoire` et éviter les fragments de mémoire inutilisables.

Le garbage collector permet de `simplifier la gestion de la mémoire` pour les programmeurs, en évitant les fuites de mémoire et en garantissant que `la mémoire est libérée de manière automatique` et efficace. Cependant, **il peut entraîner des ralentissements du programme** lorsqu'il est activé, car il doit effectuer des scans de la mémoire et des opérations de libération qui peuvent être coûteuses en termes de performance.

# Le Constructeur

En Java, un constructeur est une méthode spéciale utilisée pour initialiser les objets créés à partir d'une classe. Il porte le même nom que la classe dans laquelle il est défini et ne renvoie pas de valeur.

Lorsqu'un nouvel objet est créé à partir d'une classe, le constructeur est automatiquement appelé pour initialiser l'état initial de l'objet. Le constructeur peut prendre des paramètres pour initialiser les variables d'instance de l'objet. Si aucun constructeur n'est défini explicitement dans une classe, Java fournit un constructeur par défaut sans paramètre qui initialise toutes les variables d'instance à leurs valeurs par défaut.

Voici un exemple de définition de constructeur dans une classe Java :

```
public class Personne {
private String nom;
private int age;

    // Constructeur avec deux paramètres
    public Personne(String nom, int age) {
        this.nom = nom;
        this.age = age;
    }

    // Autres méthodes de la classe Personne...
}
```
Dans cet exemple, nous avons défini un constructeur avec deux paramètres : nom et age. Le mot-clé this est utilisé pour se référer aux variables d'instance de la classe. Lorsqu'un nouvel objet Personne est créé, le constructeur est appelé avec les valeurs des paramètres spécifiées. Par exemple :

```
Personne p1 = new Personne("Jean", 25);
```
Dans cet exemple, nous avons créé un nouvel objet Personne appelé p1 avec le nom "Jean" et l'âge 25. Le constructeur est appelé automatiquement avec ces valeurs pour initialiser les variables d'instance nom et age de l'objet p1.

En résumé, les constructeurs sont utilisés pour initialiser les objets créés à partir d'une classe en fournissant des valeurs initiales aux variables d'instance. Ils portent le même nom que la classe et ne renvoient pas de valeur. Si aucun constructeur n'est défini dans une classe, Java fournit un constructeur par défaut sans paramètre.

