# Variables en JavaScript

## Aperçu
Les variables nous permettent de stocker/garder en mémoire une valeur lors de l'exécution d'un script.  
En anglais : *Variables are labels for data values.*

## Comment déclarer une variable ?
type_de_variable nom_de_variable = valeur_de_variable
Notes :
-Les noms des variables ne doivent pas contenir de caractères spéciaux, sauf _ et $ (le symbole $ est considéré comme une lettre en JavaScript).
-En JavaScript, il n'est pas nécessaire d’ajouter un ; à la fin des lignes : l'interpréteur détecte automatiquement la fin des instructions.

Types de Données
1. Nombres
const a = 2
const b = 3.4123
const c = -509
const d = 1/3
Il est possible d’utiliser _ pour séparer visuellement les milliers :
const a = 10_000

2. Chaînes de caractères (strings)
const a = "hello world!"
const b = 'hello world!'

3. Booléens
true
false

4. Tableaux (arrays)
const table = [true, 10, 'Marc']
Accéder aux valeurs :
table[0] → true
table[1] → 10

5. Objets
const eleve = {
    clef: 'valeur',
    nom: 'Jean',
    age: 18,
    notes: [10, 4, 18]
}
Les propriétés : clef, nom, age, notes.
Accès :
eleve.nom → Jean
eleve.notes → [10, 4, 18]
eleve.notes[1] → 4
Objets contenant d'autres objets :
const eleve = {
    notes: {
        math: 18,
        francais: 14
    }
}

6. Types spéciaux
undefined : lorsqu’on essaie d’accéder à une variable ou une valeur inexistante
null : représente l’absence intentionnelle de valeur
NaN : Not a Number

Typage Faible en JavaScript
JavaScript convertit automatiquement les types si nécessaire.
const a = '1'
const b = 1

a + b  // '11' → b est converti en string
a * b  // 1   → a est converti en nombre
Exemples supplémentaires :

"Salut" * 3      // NaN
"43" > 1000      // false → 1000 est converti en chaîne et comparé alphabétiquement

## Types de Déclarations de Variables
1. const
La valeur ne peut pas être changée ni réassignée.

2. let
La valeur peut changer.

On ne peut pas redéclarer la variable.

3. var (non recommandé)
var a = 5
a = 10    // valide
let a = 10 // pas valide
Peut être redéclaré plusieurs fois.
Fonctionne différemment dans les blocs → peut causer des bugs.

4. Déclaration automatique (non recommandé)
Les variables non déclarées sont créées automatiquement lorsqu’elles sont utilisées pour la première fois.