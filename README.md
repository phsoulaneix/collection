collection
==========
1)les listes
=====================
On souhaite gérer un ensemble d'étudiants. Chaque étudiant sera défini par une classe Etudiant et devra présenter les informations suivantes:
● un matricule;
● un nom;
● une liste de notes (de taille indéfinie).
Une classe Note permettra de contenir pour chaque cours, l'intitulé du cours ainsi que la note obtenue. Les notes de chaque étudiant seront stockées dans une ArrayList.
Une méthode addNote permettant d'ajouter une note à l'étudiant sera définie.

2)Les itérateurs
=====================
On souhaite mettre en place une classe capable de réaliser des statistiques sur une collection d'objets, comme par exemple, des Etudiants, des Notes, ... Cette classe, qui sera nommée Stats, pourra ainsi calculer le maximum, le minimum et la moyenne d'une collection d'objets.
Toutes   les   classes   qui   peuvent   faire   l'objet   de   statistiques   implémenteront   une   interface Statisticable, qui est décrite comme suit:
public interface Statisticable {
public abstract float getValue();
}
Tout objet « statisticable » doit donc avoir une certaine valeur; pour un Etudiant, on choisit de prendre la moyenne de ses notes comme valeur de l'Etudiant. La classe Stats sera ensuite utilisée et donnera  pour :
● chaque étudiant:
○ sa moyenne;
○ sa meilleure note;
○ sa moins bonne note;
● chaque groupe d'étudiants:
○ la moyenne du groupe;
○ le meilleur étudiant;
○ le moins bon étudiant.


3) Le trie
=====================
On   souhaite   pouvoir   classer   la   liste   d'étudiants  suivant   le   matricule.   Pour   ce   faire,   on implémentera l'interface Comparable dans la classe Etudiant. La méthode compareTo devra donc être définie dans la classe Etudiant.
Remarque : il sera utile de se référer à la documentation en ligne pour implémenter correctement l'interface Comparable.
Une fois cela réalisé, on triera la liste d'étudiants à l'aide de la méthode Collections.sort.

4)Trie avancée
=====================
On souhaite également pouvoir trier la liste d'étudiants par moyenne et par nom.
Dans   ce   but,   deux   nouvelles   classes   (CompareMoyenne  et  CompareNom)  seront   créées   et implémenteront l'interface Comparator. Ces classes devront donc chacune définir une méthode compare prenant comme arguments les deux objets à comparer et réalisant un traitement similaire à celui de compareTo dans l'exercice précédent.
