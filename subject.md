# FIZZBUZZ in [lolcode](http://www.lolcode.org/)

Fizz buzz is a group word game for children to teach them about division.

## Rule

Players generally sit in a circle.

The player designated to go first says the number "1", and the players then count upwards in turn.

However,
- any number divisible by three is replaced by the word fizz and
- any number divisible by five by the word buzz.
- Numbers divisible by both three and five (i.e. divisible by 15) become fizz buzz.

## What you need to do

A fizzbuzz in [lolcode](https://en.wikipedia.org/wiki/LOLCODE) that print up to 100

The goal here is to learn the basic syntax of LolCode (an [esoteric programming language](https://en.wikipedia.org/wiki/Esoteric_programming_language))

- You can open the file `fizzbuzz.lolcode` and write your code in it

## Help

### The pseudo code of fizzbuzz:
```txt
for number in {0 to 100}
    if (number / 15) equal 0
        show fizz buzz
    else if (number / 3) equal 0
        show fizz
    else if (number / 5) equal 0
        show buzz
    else
        show number
    endif
endfor
```

### Run lolcode:
```bash
docker run --rm -v "$PWD":/code:ro esolang/lolcode lolcode /code/<yourfile>
```

[esolang/lolcode](https://hub.docker.com/r/esolang/lolcode)

### Keyword of lolcode:

#### Comments:
starts with `BTW`
- Example:
```
BTW im a comment
```

#### Start of file:
each file in lolcode must starts with `HAI 1.2`
- Example:
```
HAI 1.2
BTW the code here
```

#### End of file:
each file in lolcode must ends with `KTHXBYE`
- Example
```
BTW the code here
KTHXBYE
```

#### Variable:
each variable must be declared first, and after, you can put its value

to declare a variable, use `I HAS A <variable name>`

to put value in it, use `<variable name> R <value>`
- Example:
```
I HAS A variable
variable R "Hello World!"
variable R 3
```

#### Operator:
list of operators:
```
SUM OF <x> AN <y>       BTW +
DIFF OF <x> AN <y>      BTW -
PRODUKT OF <x> AN <y>   BTW *
QUOSHUNT OF <x> AN <y>  BTW /
MOD OF <x> AN <y>       BTW modulo
BIGGR OF <x> AN <y>     BTW max
SMALLR OF <x> AN <y>    BTW min
```
- Example:
```
SUM OF 4 AN 5
BTW put sum in variable
I HAS A variable
variable R SUM OF 4 an 5
```

#### Comparison
equal keyword: `BOTH SAEM <x> AN <y>`
not equal keyword: `DIFFRINT <x> AN <y>`
- Example:
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
- `UPPIN` increment by one
- `NERFIN` decrement by one
ends with `IM OUTTA YR <label>`
- Example:
```
I HAS A iii
iii R 0
IM IN YR loopten UPPIN YR iii WILE DIFFRINT iii AN 10
    VISIBLE iii
IM OUTTA YR loopten
```

### more docs: [docs](https://github.com/justinmeza/lolcode-spec/blob/master/v1.2/lolcode-spec-v1.2.md)
