---
layout: post
tags: [javascript, base]
---
```
// Commentaire JavaScript

/* Commentaire

multi ligne JavaScript */
```

## 7 types de Data différents : 
* undifined, null, boolean, string, symbol, number, object.

L'ordinateur fait la différence entre des chiffres et une chaîne de caractère.
L'ordinateur peut faire des opération mathématique sur des chiffres mais pas sur une chaîne de caractère.

Une Variable sert à stocker et manipulé une donnée en utilisant un Label qui pointe vers cette donnée au lieu d'utilisé cette donnée elle même. Les sept type de données peuvent être stockées dans une variable.

Variables sont similaires aux x et y en mathématique (c'est un simple nom pour représenter la donnée que l'on veut faire réference. La différence avec les variable mathématique, en informatique, les variables peuvent stocker différent valeurs à différent moments.

On créé ou déclare variable en ajoutant le mot var devant :
var ourName;

## Le nom d'une variable peut contenir : 
nombres lettres $  _

Mais pas d'espace ou commencé par un nombre.

# Storing Values with the Assignment Operator

[operateur](https://www.computerhope.com/jargon/o/operator.htm)

{% include tip.html content="opérateurs logique = opérateur booléen" %}

En javascript, il est possible de stocker la valeur d'une variable avec un opérateur.

Ex :
```
myVariable = 5;
```

Alloue la valeur 5 à myVariable.

{% include important.html content="Assignment fonctionne de droite à gauche, ainsi ce qui se trouve à droite de l'opérateur = est traité avant que la valeur ne soit allouée à la variable à gauche de l'opérateur." %}
```
myVar = 5;
myNum = myVar;
```

Cela alloue la valeur "5" à "myVar", ensuite résout "myVar" à "5" et l'assigne à "MyNum".

# Initializing Variables with the Assignment Operator

Il est commun d'initialisé une variable d'une valeur sur la même ligne que ça déclaration :
```
var myVar = 0;
```
Cela créé une nouvelle variable appelée myVar avec une valeur de 0.

# Understanding Uninitialized Variables

Quand une variable est déclarée, elle a une valeur initiale indéfinie (undifined). Si l'on fait une opération mathématique sur une variable undifined, le résultat sera "NaN" (Not a Number). si on concatenate une chaine de caractère (string) avec une variable undifined, le résultat sera la chaîne de caractère suivante : "undifined".

# Understanding Case Sensitivity in Variables

In JavaScript all variables and functions names are case sensitive.

## best practice :
Write variables name in camelCase (first word lowercase and first letter of each subsequent word is capitalized).

Ex:
```
var someVariable;
var anotherVariableName;
var thisVariableNameIsSoLong;
```
# Add Two Numbers with JavaScript

Number est un type de donnée en JavaScript qui représente des données numériques.

Ajouter 2 nombre avec l'opérateur + :
```
myVar = 5 + 10; // assigned 15
```

# Subtract One Number from Another with JavaScript

Soustraire un nombre d'un autre avec l'opérateur - :
```
myvar = 12 - 6; // assigned 6
```

# Multiply Two Numbers with JavaScript

Multiplier 2 nombres avec le symbol * :
```
myVar = 13 * 13; // assigned 169
```

# Divide One Number by Another with JavaScript
Diviser 2 chiffre avec le symbol / :
```
myVar = 16 / 2; // assigned 8
```

# Increment a Number with JavaScript

Increment ou ajouter "un" à une variable avec l'opérateur ++ :
```
i++;
```
Est l'équivalent de :
```
i = i + 1;
```

[Arithmetic operators - Increment (++)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Increment)

# Decrement a Number with JavaScript

Decrement  ou réduire de "un" une variable avec l'opérateur -- :
```
i--;
```
Equivalent de :
```
i = i - 1;
```

# Create Decimal Numbers with JavaScript

Il est possible de stocker des nombres décimaux en JavaScript aussi appelés floating point number ou floats.

[Plus d'info](https://en.wikipedia.org/wiki/Floating-point_arithmetic#Accuracy_problems)

# Multiply Two Decimals with JavaScript

Il est possible de faire des calculs avec des nombres décimaux :
```
var product = 2.0 * 2.5; // assigned 5
```

# Divide One Decimal by Another with JavaScript

```
var quotient = 4.4 / 2.0; // assigned 2.2
```

# Finding a Remainder in JavaScript

Le reste (remainder) de l'opérateur % donne le reste de la division de 2 nombres :

Ex:

```
5 % 2 = 1 because
Math.floor(5 / 2) = 2 (Quotient)
2 * 2 = 4
5 - 4 = 1 (Remainder)
```
En mathématique un nombre peut être soit pair (even) ou impair (odd), en le divisant par 2 :

```
17 % 2 = 1 (17 is Odd)
48 % 2 = 0 (48 is Even)
```
{% include note.html content="The remainder operator is sometimes incorrectly referred to as the \"modulus\" operator. It is very similar to modulus, but does not work properly with negative numbers." %}

# Compound Assignment With Augmented Addition

En programation, il est courant d'utiliser assignments pour modifier le contenu d'une variable.
{% include important.html content="Rappel : Tout ce qui est à droite du signe = est traité en premier" %}

```
var myVar = 1;
```

Pour ajouter 5 à myVar :

```
myVar += 5;
```

Ce qui donne :

```
console.log(myVar); // Returns 6
```

# Compound Assignment With Augmented Subtraction

-= soustrait un nombre d'une variable :

```
myVar = myVar - 5;
```

Soustrait 5 de myVar, équivalent de :

```
myVar -= 5;
```

# Compound Assignment With Augmented Multiplication

*= multiplie une variable par un nombre :

```
myVar = myVar * 5;
```

Multiplit myVar par 5, équivalent de :

```
myVar *= 5;
```

# Compound Assignment With Augmented Division

/= divise une variable par un autre nombre :

```
myVar = myVar / 5;
```

Divise myVar par 5, équivalent de :

```
myVar /= 5;
```

# Declare String Variables

Ex :

```
var myName = "your name";
```

{% include important.html content="String : série de caractère, au nombre de zéro et plus, entre guillemets (simple ou double)." %}

# Escaping Literal Quotes in Strings

Mettre un mot entre guillemets à l'intérieur d'un string en mettant un backslash :

Ex :

```
var sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```

Résultat :

Alan said, "Peter is learning JavaScript".

# Quoting Strings with Single Quotes

Il est conseiller d'utiliser soit double soit simple guillemet pour éviter errooeur de code:

Ex :

```
goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"';
badStr = 'Finn responds, "Let's go!"'; // Throws an error
```
En utilisant en premier les simples guillemets, on peut omettre les backslash en utilisant les doubles guillets ensuite :

```
var myStr = '<a href="http://www.example.com" target="_blank">Link</a>';

```

# 
