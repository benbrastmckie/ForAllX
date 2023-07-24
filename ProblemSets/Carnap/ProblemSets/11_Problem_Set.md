---
js: https://carnap.io/shared/rzach@ucalgary.ca/dark-mode.js
css: 
  - https://carnap.io/shared/rzach@ucalgary.ca/dark-mode.css
  - https://carnap.io/shared/rzach@ucalgary.ca/wideinput.css
---

# Phil 24.241 Logic I
# Problem Set \#11 Identity

####(aka I have 99 problems and each one is unique :D )

<br />

<!---

(4+6)+(4+6)+6+6+6+6+14*4  = 100

alternate would be 52+12*4

note that must use system LogicBookPDE, for identity symbols to render! LogicBookPD doesn't support identity! 

This is problem set 11 for MIT Fall 2022 Logic I, 24.241. Four of the problems come from Jtapp 303 Winter 2019 PS 8. Other five come from Zach PS9, modified for LogicBookSD system (so not allowed to ever post solutions to these!)

Description for students: Problem Set 11! Schematization in Quantifer Logic with Identity. Due Saturday, November 26th by 7pm Eastern. 

Comments to self can be entered with [blah blah]:: or [](blah blah). Former needs an empty space before the line! 

-->

To enter logical symbols logically on the logical keyboard, use:

------------------------- -----------------------------
not ~                     `-`, `~`
and &                       `&`, `/\`
or $\lor$                       `v`, `\/`
if then $\supset$                  `>`, `->`
if and only if ≡           `<>`, `<->`
universal quantifier ∀    `A`
existential quantifier ∃  `E` 
identity =                `=`
x not identical to y                `~x=y`
------------------------- -----------------------------

<br />

###Directions:

```{.QualitativeProblem .ShortAnswer points=0}
PS11.0 Just in case you worked with up to two other students on these problems, please let me know their names in the text box below. Otherwise, leave this blank and don't submit! 
```
- MEGA NOTE **READ THIS PLZ**: to say that one variable does NOT equal another, type the following: `~x = y` or `~x=y`. I can't find a not-equal symbol that works. Sorry!

When (and only when) you are happy with your answer, click the `Submit`
button. YOU CAN ONLY SUBMIT ONCE! So be careful! *Carnap* will then acknowledge and record your submission. There are **12 questions**, for a total of 100 points. 

- The first 8 have autochecker, but you can submit partial work for all but 1 $\&$ 3.
- The last four are all you. YOU GOT THIS! 

- Some of these require long disjunctions or conjunctions. *Carnap*
  will accept disjunctions or conjunctions of more than two
  disjuncts/conjuncts, e.g., it treats `(A & B & C)` as if you had
  typed `((A & B) & C)`.
- (For the "*fineprint*" directions, see a previous problem set)

[As always, you only get to submit once, and you MUST click `Submit` in order for your answer to be recorded.]::


### Before you leave this page, make sure every problem which you have solved correctly is also `submit`ted!

<br />

###Problems 1 through 2! 

- **Universe of Discourse** (UD): all currently living people (YOLO!), including in particular `**b**', denoting Barbara (Streisand) 


**Predicate schemas**:

- $Ey$:	$y$ will travel to Europe.   
- $Py$:	$y$ will travel to Portugal.         
- $Hx$:	$x$ will stay home (lame!).     
- $Vxy$:	$x$ will visit $y$.         

<br />

[note that Carnap also accepts the following, since quantifiers commute across a conditional when in the consequent: 
(Ax)(Ey)((Ex > (Vxb &(~Vyb & ~y=x))))   ]::

[JTapp PS8 3a]::

~~~{.Translate .FOL system="LogicBookPDE" points=4}
PS11.1 (Ax)(Ex > (Vxb & (Ey)(~Vyb & ~y=x))) : Any person will travel to Europe only if that person visits Barbara and a different person doesn't visit Barbara.
~~~

[easy one! so include. can also have it in the form (Ax)(Px > (Ey)(Ez)((~Ey & ~Ez & ~x=y & ~x=z) )). Since the quantifiers commute across conditional when in the CONSEQUENT. 
So carnap also accepts the following:
(Ax)(Px > (Ey)(Ez)((~Ey & ~Ez & ~x=y & ~x=z)) )  ]::

[JTapp PS8 3d]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam" points=6}
PS11.2 (Ax)(Ey)(Ez)(Px > (~Ey & ~Ez & ~x=y & ~x=z) ), (Ax)(Ey)(Ez)(Px > (~Ey & ~Ez & ~x=y & ~x=z & ~y=z) ) : For everyone who visits Portugal, there are two other people that don't visit Europe.
~~~



###The rest of the problems (12 total)!  



**Solar system of Discourse**: celestial objects in the solar system

------------- ----------------------- ------------- --------
**$Ax$**:         $x$ is an asteroid.      **$e$**:           Earth
**$Mx$**:         $x$ is a moon.            **$m$**:           Mars
**$Px$**:         $x$ is a planet.         **$j$**:                Jupiter
**$Oxy$**:       $x$ orbits $y$.	       **$i$**:           Io
**$Tx$**:     $x$ has an atmosphere.
**$Lxy$**:     $x$ is larger than $y$.
------------- ----------------------- ------------- --------

Symbolize the following sentences using the above symbolization key, repeated at points below for your viewing convenience. 


[Zach PS9.1 ]::

~~~{.Translate .FOL system="LogicBookPDE" points=4}
PS11.3 (Ax)(~x=m -> Tx) : Every celestial body other than Mars has an atmosphere.
~~~

[Zach PS9.2 ]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam" points=6}
PS11.4 (Ex)(Ey)(~x=y /\ Ax /\ Ay /\ Oxy)  : Some asteroid orbits another.
~~~

[Zach PS9.3 ]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam" points=6}
PS11.5 (Ex)(Px /\ (Ay)((Py /\ ~x=y) -> Lxy)) : Some planet is larger than every other planet.
~~~

(Hint for the next one: Remember that "except for" leaves open whether Io has an atmosphere; the sentence does not entail that Io necessarily lacks an atmosphere)

[Zach PS9.4 ]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam" points=6}
PS11.6 (Ax)((Mx /\ Oxj /\ ~x = i) -> Tx), (Ax)((Mx /\ Oxj /\ ~x = i) -> Tx) /\ Mi /\ Oij : Except for Io, all of Jupiter's moons have an atmosphere.
~~~


**UD**: celestial objects in the solar system

------------- ----------------------- ------------- --------
**$Ax$**:         $x$ is an asteroid.      **$e$**:           Earth
**$Mx$**:         $x$ is a moon.            **$m$**:           Mars
**$Px$**:         $x$ is a planet.         **$j$**:                Jupiter
**$Oxy$**:       $x$ orbits $y$.	       **$i$**:           Io
**$Tx$**:     $x$ has an atmosphere.
**$Lxy$**:     $x$ is larger than $y$.
------------- ----------------------- ------------- --------

## "Only"

[Zach PS9.5 ]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam" points=6}
PS11.7 Tm /\ Te /\ (Ax)(Tx -> (x=m \/ x=e)), (Ax)(Tx <-> (x=m \/ x=e)) : Only Mars and Earth have an atmosphere.
~~~

- For a future problem(set): "Only that which is truly yourself has the power to heal." --Carl Jung

[seems like comma between sentences allows you to include two logically distinct answers as correct; so that's neat! way to assign problems where there are ambiguities]::



## Uniqueness

[Zach PS9.7 ]::

~~~{.Translate .FOL system="LogicBookPDE" points=6}
PS11.8 (Ex)(Mx /\ Oxe /\ (Ay)((My /\ Oye) -> y=x)), (Ex)(Ay)((My /\ Oye) <-> y=x) : Earth has only one moon.
~~~

- Or as the philosophers say: "we are all disturbed in our own special way."

## Numerical quantification (and turning off auto-checker)

**UD**: celestial objects in the solar system

------------- ----------------------- ------------- --------
**$Ax$**:         $x$ is an asteroid.      **$e$**:           Earth
**$Mx$**:         $x$ is a moon.            **$m$**:           Mars
**$Px$**:         $x$ is a planet.         **$j$**:                Jupiter
**$Oxy$**:       $x$ orbits $y$.	       **$i$**:           Io
**$Tx$**:     $x$ has an atmosphere.
**$Lxy$**:     $x$ is larger than $y$.
------------- ----------------------- ------------- --------

- Remember that "two moons" means "at least two", not "exactly two". (Remember that someone is gonna ask you this 10 years from now. Hint: it's not gonna be me!)

- No auto-checker for the rest! 


[Zach PS9.9 ]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam nocheck" points=14}
PS11.9 (Ex)(Ey)(~x=y /\ Mx /\ Oxm /\ My /\ Oym) : Mars has two moons.
~~~

[Zach PS9.11]::

[neat student idea (AK): do disjunction of no moons, exactly one, exactly two. in principle this should work! so bummer that carnap says not equivalent:

(Ax)(~(Mx & Oxm)) v (Ex)(Az)(Mx & Oxm & (~x=z > ~(Mz & Ozm))) v (Ex)(Ey)(Az)(Mx & My & Oxm & Oym & ((~x=z & ~y=z) > ~(Mz & Ozm)))]::

[does this solN work??? check truth conditions/countermodels. 

it might work!

(Az)(Ex)(Ey)((Mz & Ozm) > (z=x v z=y))]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam nocheck" points=14}
PS11.10 ~(Ex)(Ey)(Ez)(Mx /\ Oxm /\ My /\ Oym /\ Mz /\ Ozm /\ ~x=y /\ ~x=z /\ ~y=z) : Mars has at most two moons.
~~~

[Zach PS9.12 ]::

[ben chen idea, that seems legit: say that there are at least two moons w/ atmosophere and at most two: 

(Ex)(Ey)(~x=y & Mx & My & Tx & Ty) & ~(Ex)(Ey)(Ez)(~x=y & ~x=z & ~y=z & Mx & My & Mz & Tx & Ty & Tz) ]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam nocheck" points=14}
PS11.11 (Ex)(Ey)(~x=y /\ Mx /\ Tx /\ My /\ Ty /\ (Az)((Mz /\ Tz) -> (z = x \/ z = y))), (Ex)(Ey)(~x=y /\ (Az)((Mz /\ Tz) <-> (z = x \/ z = y))) : There are exactly two moons with an atmosphere.
~~~

Remember that "x has an atmosphere" is `Tx` not `Ax`.



## Definite descriptions

- Remember that **singular** possessives like "Earth's moon" can be
interpreted like the definite description "the moon of Earth."  But
**plural** possessives like "Mars's moon**s**" aren't definite
descriptions.


[Zach PS9.14]::

[interesting alternative solN:
(Ex)(Ay)(Mx & Oxe & (Az)((Mz & Oze) > z=x) & ((My & Oym) > Lxy))]::

~~~{.Translate .FOL system="LogicBookPDE" options="exam nocheck" points=14}
PS11.12 (Ex)(((Mx /\ Oxe) /\ (Ay)((My /\ Oye) ->x=y)) /\ (Az)((Mz /\ Ozm)-> Lxz)),(Ex)(Ay) ( ( (My /\ Oye) <->x=y) /\ (Az) ( (Mz /\ Ozm)-> Lxz) ) : Earth's moon is larger than Mars's moons.
~~~


**UD**: celestial objects in the solar system

------------- ----------------------- ------------- --------
**$Ax$**:         $x$ is an asteroid.      **$e$**:           Earth
**$Mx$**:         $x$ is a moon.            **$m$**:           Mars
**$Px$**:         $x$ is a planet.         **$j$**:                Jupiter
**$Oxy$**:       $x$ orbits $y$.	       **$i$**:           Io
**$Tx$**:     $x$ has an atmosphere.
**$Lxy$**:     $x$ is larger than $y$.
------------- ----------------------- ------------- --------

<br />

### Before you leave this page, make sure every problem which you have solved correctly is also submitted! 
#####And make sure you've reflected on at least one thing you're grateful for! I'm grateful for *Carnap*!