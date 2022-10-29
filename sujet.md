# FIZZBUZZ dans [lolcode](http://www.lolcode.org/)

Fizz buzz est un jeu de mots collectif destiné aux enfants pour leur apprendre la division.


## Règle

Les joueurs sont généralement assis en cercle.

Le joueur désigné pour commencer dit le chiffre "1", et les joueurs comptent ensuite vers le haut à tour de rôle.

Toutefois,
- tout nombre divisible par trois est remplacé par le mot "fizz" et
- tout nombre divisible par cinq par le mot buzz.
- Les nombres divisibles à la fois par trois et par cinq (c'est-à-dire divisibles par 15) deviennent fizz buzz.


## Ce que vous devez faire

Un fizzbuzz en [lolcode](https://en.wikipedia.org/wiki/LOLCODE) qui affiche jusqu'à 100.

Le but ici est d'apprendre la syntaxe de base du LolCode (un [langage de programmation ésotérique](https://en.wikipedia.org/wiki/Esoteric_programming_language)).

- Tu peux ouvrir le fichier `fizzbuzz.lolcode` et ecrire ton code dedans

## Aide

### Le pseudo-code de fizzbuzz:
```txt
pour nombre dans {0 à 100}
    si (nombre / 15) égal 0
        affiche le buzz fizz
    sinon if (number / 3) equal 0
        afficher fizz
    sinon si (nombre / 5) égal à 0
        afficher le buzz
    sinon
        affiche le numéro
    fin si
fin pour
```

### Lancer du lolcode:
```bash
docker run --rm -v "$PWD":/code:ro esolang/lolcode lolcode /code/<ton fichier>
```

### Mot clé du lolcode:

#### Commentaires :
commence par `BTW`
- Exemple :
```
BTW je suis un commentaire
```

#### Début du fichier:
chaque fichier dans lolcode doit commencer par `HAI 1.2`.
- Exemple :
```
HAI 1.2
BTW le code ici
```

#### Fin de fichier:
Chaque fichier de lolcode doit se terminer par `KTHXBYE`.
- Exemple
```
BTW le code ici
KTHXBYE
```

#### Variable :
chaque variable doit être déclarée en premier, et après, vous pouvez mettre sa valeur

Pour déclarer une variable, utilisez `I HAS A <nom de la variable>`.

pour y mettre une valeur, utilisez `<nom de la variable> R <valeur>`
- Exemple :
```
I HAS A variable
variable R "Hello World !"
variable R 3
```

#### Opérateur :
liste d'opérateurs :
```
SUM OF <x> AN <y>       BTW +
DIFF OF <x> AN <y>      BTW -
PRODUKT OF <x> AN <y>   BTW *
QUOSHUNT OF <x> AN <y>  BTW /
MOD OF <x> AN <y>       BTW modulo
BIGGR OF <x> AN <y>     BTW max
SMALLR OF <x> AN <y>    BTW min
```
- Exemple :
```
SUM OF 4 AN 5
BTW met la somme dans une variable
I HAS A variable
variable R SUM OF 4 an 5
```

#### Comparaison
mot-clé égal : `BOTH SAEM <x> AN <y>`
mot-clé non égal : `DIFFRINT <x> AN <y>`
- Exemple :
```
I HAS A variable
variable R 5
I HAS A var
var R 4
BOTH SAEM variable AN var
DIFFRINT variable AN var
```

#### Input/Output (get from user / show to user)
output/print/show: `VISIBLE <x>`
input/get: `GIMMEH <variable name>`
- Exmaple
```
I HAS A var
GIMMEH var
VISIBLE var
```

#### Condition
use a comparison, followed by `O RLY?` and `YA RLY` (if) `MEBBE` (else if) `NO WAY` (else) and end it with `OIC`
- Example
```
BOTH SAEM 4 AN 4
O RLY?
    YA RLY
        VISIBLE "yes"
    NO WAI
        VISIBLE "false"
OIC
```
```
BOTH SAEM 4 AN 5
O RLY?
    YA RLY
        VISIBLE "yes"
    MEBBE BOTH SAEM 3 AN 3
        VISIBLE "3 == 3"
    NO WAI
        VISIBLE "false"
OIC
```

#### While/For
starts with `IM IN YR <label> <operation> YR <variable> WILE <expression>`
`<label>` is the loop name
`<operation>` can be:
- `UPPIN` augmente de un la variable
- `NERFIN` enleve un à la variable
ends with `IM OUTTA YR <label>`
- Example:
```
I HAS A iii
iii R 0
IM IN YR loopten UPPIN YR iii WILE DIFFRINT iii AN 10
    VISIBLE iii
IM OUTTA YR loopten
```

### plus de docs : [docs](https://github.com/justinmeza/lolcode-spec/blob/master/v1.2/lolcode-spec-v1.2.md)
