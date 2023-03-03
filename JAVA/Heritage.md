# Heritage 
L'héritage est un concept clé de la programmation orientée objet (POO) qui permet de définir une nouvelle classe à partir d'une classe existante, appelée classe parent ou superclasse. En Java, l'héritage est implémenté à l'aide du mot-clé "extends".

Pour utiliser l'héritage en Java, vous pouvez créer une nouvelle classe qui étend une classe existante en utilisant le mot-clé "extends" suivi du nom de la classe parent. La nouvelle classe est alors appelée sous-classe ou classe fille, et la classe parent est appelée superclasse ou classe mère.

Lorsque vous créez une sous-classe, elle hérite de toutes les propriétés et méthodes publiques et protégées de sa classe parent. Cela signifie que la sous-classe peut accéder à ces propriétés et méthodes directement, sans avoir besoin de les redéfinir. Cela permet de réutiliser facilement le code et d'éviter la duplication.

En plus d'hériter des propriétés et méthodes de la classe parent, une sous-classe peut également ajouter ses propres propriétés et méthodes. Elle peut également redéfinir ou remplacer les méthodes de la classe parent en utilisant le même nom de méthode mais en fournissant une implémentation différente.

L'héritage peut également être utilisé pour créer une hiérarchie de classes, où chaque classe fille ajoute de nouvelles fonctionnalités et propriétés à la classe parent. Par exemple, vous pouvez créer une classe "Animal" qui définit les propriétés et méthodes communes à tous les animaux, puis créer des classes filles telles que "Chien" et "Chat" qui ajoutent des propriétés et méthodes spécifiques à ces animaux.

En résumé, l'héritage en Java permet de créer de nouvelles classes à partir d'une classe existante en utilisant le mot-clé "extends". La sous-classe hérite de toutes les propriétés et méthodes publiques et protégées de sa classe parent, et peut ajouter ses propres propriétés et méthodes, ainsi que redéfinir les méthodes de la classe parent. L'héritage peut également être utilisé pour créer une hiérarchie de classes.

Voici un exemple de code Java qui illustre l'héritage :

```
// La classe parent
class Vehicule {
protected String marque; // propriété protégée (accessible depuis les classes filles)
private int annee; // propriété privée (non accessible depuis les classes filles)

    // constructeur de la classe parent
    public Vehicule(String marque, int annee) {
        this.marque = marque;
        this.annee = annee;
    }
    
    // méthode publique de la classe parent
    public void demarrer() {
        System.out.println("Le véhicule démarre.");
    }
    
    // méthode protégée de la classe parent
    protected void arreter() {
        System.out.println("Le véhicule s'arrête.");
    }
}

// La sous-classe qui hérite de Vehicule
class Voiture extends Vehicule {
private String modele; // propriété privée

    // constructeur de la sous-classe
    public Voiture(String marque, int annee, String modele) {
        super(marque, annee); // appel du constructeur de la classe parent
        this.modele = modele;
    }
    
    // méthode publique de la sous-classe
    public void klaxonner() {
        System.out.println("La voiture klaxonne.");
    }
    
    // méthode qui redéfinit la méthode de la classe parent
    @Override
    public void demarrer() {
        System.out.println("La voiture démarre en appuyant sur le bouton.");
    }
}

// Utilisation des classes
public class Main {
public static void main(String[] args) {
// création d'une instance de la sous-classe Voiture
Voiture maVoiture = new Voiture("Renault", 2020, "Clio");

        // utilisation des méthodes de la classe parent
        maVoiture.demarrer(); // affiche "La voiture démarre en appuyant sur le bouton."
        maVoiture.arreter(); // propriété protégée, accessible uniquement depuis la classe fille
        
        // utilisation des méthodes de la sous-classe
        maVoiture.klaxonner(); // affiche "La voiture klaxonne."
    }
}
```
Dans cet exemple, la classe Vehicule est la classe parent et la classe Voiture est la sous-classe qui hérite de Vehicule. La classe Vehicule a deux propriétés, marque (protégée) et annee (privée), et deux méthodes, demarrer() (publique) et arreter() (protégée). La classe Voiture ajoute une propriété modele (privée) et une méthode klaxonner() (publique), et redéfinit la méthode demarrer() de la classe parent.

Dans la méthode main(), nous créons une instance de la sous-classe Voiture en utilisant le constructeur de la sous-classe. Nous utilisons ensuite les méthodes de la classe parent et de la sous-classe pour démarrer la voiture, l'arrêter et la faire klaxonner. Notez que la méthode arreter() de la classe parent est protégée, ce qui signifie qu'elle n'est accessible que depuis la sous-classe Voiture.
