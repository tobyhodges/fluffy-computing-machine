---
title: "Cat? Fact!"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is `cowsay`?
- How do you get a random cat fact?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Introduce the {cowsay} package
- Get a random fact

::::::::::::::::::::::::::::::::::::::::::::::::

## All About Cats

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: instructor

When people view this lesson on their own computer, the kittens will be
different because they are coming from placekitten, which is an outside
resource that sends a random kitten.

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::


Cats are incredible creatures with very soft fur and pointy fingers.

![Murderfloof](https://placekitten.com/600/800){alt='a cute image of a kitten'}

But did you know:



```{.output}

 -------------- 
The largest breed of cat is the Ragdoll with males weighing in at 1 5 to 20 lbs. The heaviest domestic cat on record was a neutered male tabby named Himmy from Queensland, Australia who weighed 46 lbs. 1 5 oz. 
 --------------
    \
      \
        \
            |\___/|
          ==) ^Y^ (==
            \  ^  /
             )=*=(
            /     \
            |     |
           /| | | |\
           \| | |_|/\
      jgs  //_// ___/
               \_)
  
```

Now you know!

## Cowsay

The [cowsay program](https://en.wikipedia.org/wiki/Cowsay) was an joke program
that programmers would use to display a cartoon animal (initially a cow, but 
soon many other variants emerged) saying anything that you gave it. In 2015, 
Scott Chamberlain ported this program to the R package with the same name, so
that you too could write silly
[ASCII](https://glosario.carpentries.org/en/#ASCII) art cartoons in R:


```r
library(cowsay)
say("What's the status, _Felis catus_?", by = "cow")
```

```{.output}

 ----- 
What's the status, _Felis catus_? 
 ------ 
    \   ^__^ 
     \  (oo)\ ________ 
        (__)\         )\ /\ 
             ||------w|
             ||      ||
```

::::::::::::::::::::::::::::::::::::: discussion

### Inaccessibility of ASCII art

ASCII art (art made from arranging text characters on a screen) can be fun if
you are sighted, but if you rely on a screen reader to navigate your computer
and the web, ASCII art is inaccessible. To a screen reader, the cow above
looks nothing like a cow:

> ` \n ----- \nWhat's the status, _Felis catus_? \n ------ \n    \   ^__^ \n     \  (oo)\ ________ \n        (__)\         )\ /\ \n             ||------w|\n             ||      || `


ASCII art should never be used in official lessons. This is a lesson for a small
team and is not intended to be shared more broadly.

::::::::::::::::::::::::::::::::::::::::::::::::

## Just the facts

Cat Facts come from [The Cat Fact API](https://catfact.ninja/), which provides
a way for programs like R to get a random fact from the internet.

To get a cat fact from {cowsay}, you need two additional things:

1. an internet connection
2. the {curl} package

:::::: callout

### Why use the {curl} package?

The {curl} package is an R package that wraps the popular command line tool for
accessing [APIs (Application Programming Interfaces)](https://glosario.carpentries.org/en/#api). We use it to get cat facts from the catfact API, but it is a very powerful
package that we can also use to interact with GitHub and other services.

::::::::::::::

You can install the {curl} package by using `install.packages()`:


```r
install.packages("curl")
```

Once you have that, we can use this to get a new cat fact:


```r
library("cowsay")
library("curl")
say("catfact")
```

```{.output}

 -------------- 
A cat's appetite is the barometer of its health. Any cat that does not eat or drink for more than two days should be taken to a vet. 
 --------------
    \
      \
        \
            |\___/|
          ==) ^Y^ (==
            \  ^  /
             )=*=(
            /     \
            |     |
           /| | | |\
           \| | |_|/\
      jgs  //_// ___/
               \_)
  
```



::::::::::::::::::::::::::::::::::::: keypoints 

- The {cowsay} package provides ASCII animals with text
- ASCII is inherently inaccessible
- The {cowsay} package can provide random cat facts

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
