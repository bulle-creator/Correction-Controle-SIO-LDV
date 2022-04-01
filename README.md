# Correction-Controle-SIO-LDV

<img width="456" alt="Capture" src="https://user-images.githubusercontent.com/77787321/160827298-ff0f2e60-7667-43ed-8a2d-5b3282204592.PNG">

### Un chenil héberge des animaux domestiques. 
#### Règle A :Tout  animal domestique est associé, au plus, à un propriétaire (nom + coordonnées), à un chenil et à une liste de nourritures admises.   
P-1 : Le diagramme est-il fidèle à la règle A ? Justifier

Oui car il est relié à une instance de Personne (proprio) et la multiplicité est de 0 à 1.

P-2 : On souhaite ajouter à la classe Personne la méthode isProprio() qui permettra de savoir si une personne est responsable (propriétaire) d’au moins un animal ou non. Donner le code de cette méthode 

```
 fonction isProprio : boolean {
  return this.animaux.size > 0 ;
 }
```
P-3 : On souhaite pouvoir enregistrer, pour un animal donné, ses types de nourriture préférés parmi lesquels il a droit. Faire évoluer le diagramme UML en conséquence.

<img width="456" alt="Capture - Copie (2)" src="https://user-images.githubusercontent.com/77787321/161099372-db230902-5e68-4faf-b8ca-7365f02c870b.PNG">

Soit felix, le nom d’une variable qui référence à une instance de Chat, dans un programme qui exploite le modèce ci-dessus.
Felix-1 : Donner l’instruction qui permet de connaître le nom de (lobjet référencé par) felix. 
```
  felix.getNom();
```
Felix-2 : Définir une fonction nommé getNomProprio() dans AnimalDomestique, dans le but de connaître le nom de son éventuel propriétaire. Appliquez le à felix.
```
fonction getNomProprio() String {
  if (this.proprio != null ){
    return this.proprio.getNom();
    }
   return "";
  }
```
Felix-3 :Donner l’instruction qui permet de connaître l’espérance de vie représentée par l’objet référencé par felix.

``` 
felix.esperenceDeVie()
```
Soit rex, le nom d’une variable qui référence une instance de Chien, dans un programme qui exploite le modèce ci-dessus.
Rex-1 :Donner l’instruction qui permet de connaître le nombre de types de nourriture admises pour (lobjet référencé par) rex
```
Rex.getNourritureAdmise()
```
Rex-2 : Donner l’instruction qui affiche les types de nourriture qui lui sont permis.
```
for (Type.Nourriture n : rex getNourritureAdmise() )
  print (n.getLibellé)
```
Rex-3 : Donner l’instruction qui permet de connaître son espérance de vie. 
```
Rex.esperenceDeVie()
```
Soit bob, le nom d’une variable qui référence une instance de Personne, dans un programme qui exploite toutjours le même modèce. 

Bob-1 : Donner l’instruction qui affiche les animaux dont bob a la charge.  

```
for (AnimalDomestique a : bob.getAnimaux() {
  print (a);
```
Bob-2 : Donner l’instruction qui affiche les chats de bob. 

On pourra utiliser l’opérateur instanceof présent dans la plupart des langages.

Exemples :  
String x = "coucou";

* x instanceof String  (rend true)  
* x instanceof Object  (rend true, car Object est la classe mère de String)    
* x instanceof Integer (rend false)  
```
for (AnimauxDomestique a : bob.getAnimaux() {
  if (a instanceof Chat)
    print (a);
```
### Bonus: On souhaite pouvoir montre aux Propriétaire si leur animaux on des maladies. Fait évoluer le diagramme UML..
 
<img width="434" alt="Capture1" src="https://user-images.githubusercontent.com/77787321/161289195-da3e8461-02f5-45ee-a7fd-1a472d6eac07.PNG">

