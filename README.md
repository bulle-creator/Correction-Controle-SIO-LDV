# Correction-Controle-SIO-LDV

<img width="456" alt="Capture" src="https://user-images.githubusercontent.com/77787321/160827298-ff0f2e60-7667-43ed-8a2d-5b3282204592.PNG">

_Un chenil héberge des animaux domestiques._   
_Règle A :Tout  animal domestique est associé, au plus, à un propriétaire (nom + coordonnées), à un chenil et à une liste de nourritures admises._   
_P-1 : Le diagramme est-il fidèle à la règle A ? Justifier_

Oui car il est relié à Proprio et la multiplicité est de 0 à 1.

_P-2 : On souhaite ajouter à la classe Personne la méthode isProprio() qui permettra de savoir si une personne est responsable (propriétaire) d’au moins un animal ou non. Donner le code de cette méthode_ 

```
 fonction isProprio : boolean {
  return this.Animaux length > 0 ;
 }
```
_P-3 : On souhaite pouvoir enregistrer, pour un animal donné, ses types de nourriture préférés parmi lesquels il a droit. Faire évoluer le diagramme UML en conséquence._

 image

_ Soit felix, le nom d’une variable qui référence à une instance de Chat, dans un programme qui exploite le modèce ci-dessus. _
_Felix-1 : Donner l’instruction qui permet de connaître le nom de (lobjet référencé par) felix._ 
```
Chat felix;
  felix : get.Nom();
```
_Felix-2 : Définir une fonction nommé getNomPropro() dans AnimalDomestique, dans le but de connaître le nom de son éventuel propriétaire. Appliquez le à felix. _
```
fonction get.Nom() String {
  if (this.proprio != null ){
    return this.prorio.get.Nom();
    }
   return "";
  }
```
_Felix-3 :Donner l’instruction qui permet de connaître l’espérance de vie représentée par l’objet référencé par felix. _

``` 
felix.EsperenceDeVie()
```
_Soit rex, le nom d’une variable qui référence une instance de Chien, dans un programme qui exploite le modèce ci-dessus._ 
_Rex-1 :Donner l’instruction qui permet de connaître le nombre de types de nourriture admises pour (lobjet référencé par) rex_
```
Rex.get.NourritureAdmise()get()
```
_Rex-2 : Donner l’instruction qui affiche les types de nourriture qui lui sont permis. _
```
for (Type.Nourriture n : rex)
  print (n :get.libellé)
```
Rex-3 : Donner l’instruction qui permet de connaître son espérance de vie. 
```
Rex.EsperenceDeVie()
__
```
_Soit bob, le nom d’une variable qui référence une instance de Personne, dans un programme qui exploite toutjours le même modèce. 

 
Bob-1 : Donner l’instruction qui affiche les animaux dont bob a la charge. 
Bob-2 : Donner l’instruction qui affiche les chats de bob. 

_On pourra utiliser l’opérateur instanceof présent dans la plupart des langages._ 

_Exemples :_ 

_String x = "coucou";_ 

_x instanceof String  (rend true)_ 
_x instanceof Object  (rend true, car Object est la classe mère de String)_ 
_x instanceof Integer (rend false)_
```
for (AnimauxDomestique a : bob get.Animaux() {
  if (a instanceof Chat)
    print (a);
```
_Bonus: On souhaite pouvoir montre aux Propriétaire si leur animaux on des maladies. Fait évoluer le diagramme UML.._
 
