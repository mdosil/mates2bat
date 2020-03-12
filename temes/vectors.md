#Tema 7: Vectors a l'espai

El [curs passat](http://mdosil.cat/mates1batcientific/temes/vectors/) /estudiàvem/ la geometria en el pla, $\mathbb{R}^2$. Aquest any, l'estudiarem a l'espai, $\mathbb{R}^3$. Això vol dir que a part dels punts, vectors i rectes també treballarem amb plans.

L'espai $\mathbb{R}^3$ té 3 dimensions, les anomenarem $x$, $y$ i $z$ i representarem els objectes en aquests eixos coordenats.

<iframe scrolling="no" title="Eixos a l'espai R3" src="https://www.geogebra.org/material/iframe/id/gsFAvcep/width/495/height/624/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="495px" height="624px" style="border:0px;"> </iframe>



##Punts a l'espai

Un punt a l'espai té 3 coordenades. Per exemple, el punt $P(2,3,5)$ es representa de la manera següent:

<iframe scrolling="no" title="Punt a R3" src="https://www.geogebra.org/material/iframe/id/ESxs9WnF/width/495/height/500/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="495px" height="500px" style="border:0px;"> </iframe>

##Vectors a l'espai

Donats 2 punts a l'espai, $A$ i $B$, definim el vector $\vec{ AB}$ d'origen $A$ i extrem $B$ com un segment en l'espai que determina una *direcció*, un *mòdul* i un *sentit*.

Les coordenades del vector $\vec{AB}$ i el seu mòdul es calculen segons:
\begin{align}
A&=(a_1,a_2,a_3)\\
B&=(b_1,b_2,b_3)\\
\vec{AB}&=(b_1-a_1,b_2-a_2,b_3-a_3)\\
|\vec{AB}|&=\sqrt{(b_1-a_1)^2 + (b_2-a_2)^2+ (b_3-a_3)^2}
\end{align}

Dos vectors són __equipol.lents__ si tenen el mateix mòdul, la mateixa direcció i el mateix sentit. El conjunt format per tots els vectors equipol.lents s'anomena __vector lliure__. Normalment, el representant del vector lliure que s'utilitza és el que té origen a l'origen de coordenades $O=(0,0,0)$ i extrem a un punt $P$. Les coordenades del vector lliure doncs, coincideixen amb les coordenades del punt $P$.

<iframe scrolling="no" title="Vector a R3" src="https://www.geogebra.org/material/iframe/id/UH6M7UGj/width/600/height/500/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="500px" style="border:0px;"> </iframe>



##Operacions amb vectors

Les operacions amb vectors en l'espai són similars a les que definíem amb els [vectors en el pla](http://mdosil.cat/mates1batcientific/temes/vectors/#operacions-amb-vectors). Aquí però definirem un producte més, el producte vectorial, que descobrirem tot seguit.



###Suma

Definim la suma de dos vectors $\vec{u}=(u_1,u_2,u_3)$ i $\vec{v}=(v_1,v_2,v_3)$ com la operació:

$$\vec{u}+\vec{v}=(u_1+v_1,u_2+v_2,u_3+v_3)$$

La suma de dos vectors compleix la _regla del paral.lelogram_ tal i com vam veure amb la suma de vectors en el pla.

<iframe scrolling="no" title="Suma de vectors a R3" src="https://www.geogebra.org/material/iframe/id/SC6YUDJf/width/600/height/709/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="709px" style="border:0px;"> </iframe>

####Propietats

* Commutativa: $\overrightarrow{u}+\overrightarrow{v}=\overrightarrow{v}+\overrightarrow{u}$
* Associativa: $(\overrightarrow{u}+\overrightarrow{v})+\overrightarrow{w}=\overrightarrow{u}+(\overrightarrow{v}+\overrightarrow{w})$
* Element neutre: $\overrightarrow{u}+\overrightarrow{0}=\overrightarrow{u}$
* Element oposat: $\overrightarrow{u}+(-\overrightarrow{u})=\overrightarrow{0}$

La resta de dos vectors s'entén com la suma d'un vector i l'oposat d'un altre, per tant, conserva les mateixes propietats.

###Producte d'un vector per un nombre real

Sigui $k$ un nombre real diferent de zero i $\overrightarrow{ u }$ un vector a $\mathbb{ R }^3$, el producte de $k$ per $\overrightarrow{ u }$ és un altre vector de components:

$$\overrightarrow{ u }=(u_1,u_2,u_3)\rightarrow k\cdot \overrightarrow{ u }=(k\cdot u_1,k\cdot u_2, k\cdot u_3)$$

Per tant, $k\cdot \overrightarrow{ u }$ té la mateixa direcció que el vector $\overrightarrow{ u }$ i el sentit dependrà de si $k$ és un nombre positiu o negatiu. Pel que fa al mòdul: $|k\cdot \overrightarrow{ u }|=|k|\cdot |\overrightarrow{ u }|$.

El producte d'un vector per un nombre real ens permet obtenir vectors __unitaris__, de mòdul $1$: una manera senzilla d'obtenir un vector unitari a partir d'un de donat, és dividir les seves components pel mòdul del vector. Si $\overrightarrow{ u }$ és un vector qualsevol, $\frac{ 1 }{ |\overrightarrow{ u }| }\cdot \overrightarrow{ u }$ té mòdul 1.

####Propietats


* Associativa: $a\cdot (b\cdot \overrightarrow{u})=(a\cdot b)\cdot \overrightarrow{u}$
* Distributiva respecte escalars: $(a + b)\cdot \overrightarrow{u}=a\cdot \overrightarrow{u}+b\cdot \overrightarrow{u}$
* Distributiva respecte vectors: $a\cdot (\overrightarrow{u}+\overrightarrow{ v })=a\cdot \overrightarrow{u}+b\cdot \overrightarrow{v}$
* Element neutre: $\overrightarrow{u}\cdot 1=\overrightarrow{u}\cdot 1 = \overrightarrow{u}\$

##Espais vectorials

Direm que un conjunt $E$ qualsevol és un espai vectorial sobre un cos $K$ si estan definides les operacions:

* Una operació interna (suma):

    \begin{align}
    (E,E)&\rightarrow E\\
    (\overrightarrow{ u },\overrightarrow{ v })&\rightarrow \overrightarrow{ u }+\overrightarrow{ v }
    \end{align}

* Una operació externa (producte per un escalar)

\begin{align}
(K , E) &\rightarrow E \\
(k,\overrightarrow{ u })&\rightarrow k\cdot \overrightarrow{ u }
\end{align}

i a més es compleixen les propietats següents:

* Distributiva respecte escalars: $(a + b)\cdot \overrightarrow{u}=a\cdot \overrightarrow{u}+b\cdot \overrightarrow{u}$
* Distributiva: $a\cdot (\overrightarrow{u}+\overrightarrow{ v })=a\cdot \overrightarrow{u}+a\cdot \overrightarrow{v}$
* Associativa: $a\cdot (b\cdot \overrightarrow{u})=(a\cdot b)\cdot \overrightarrow{u}$
* Element neutre: $\overrightarrow{u}\cdot 1=\overrightarrow{u}\cdot 1 = \overrightarrow{u}\$

El conjunt de vectors a $\mathbb{R}^3$ sobre el cos dels nombres reals $\mathbb{R} $, amb les operacions de suma i producte per un escalar formen un __Espai Vectorial__.


###Combinació lineal de vectors

Donat un conjunt de vectors de l'espai vectorial $\mathbb{R}^3$, $\{\overrightarrow{ u }_1,\overrightarrow{ u }_2, \overrightarrow{ u }_3,...,\overrightarrow{ u }_n \}$, direm que un vector $\overrightarrow{ v }$ és una __combinació lineal__ de tots ells si es pot expressar de la manera següent:

$$\overrightarrow{ v }=\lambda _1 \overrightarrow{ u }_1+\lambda _2 \overrightarrow{ u }_2+\lambda _3 \overrightarrow{ u }_3+...+\lambda _n \overrightarrow{ u }_n $$

amb


$$\lambda _1, \lambda _2, ... \lambda _n \in \mathbb{R}$$

Per exemple el vector $\overrightarrow{ u }=(8,0,11)$ és combinació lineal dels vectors $\overrightarrow{ a }=(1,0,1)$ i $\overrightarrow{ b }=(2,0,3)$ ja que:

$$(8,0,11)=2(1,0,1)+3(2,0,3)$$

Si un vector ha de ser combinació lineal d'un altre vector, necessàriament hauran de ser múltiples.

Un altre exemple de combinació lineal de vectors és la diagonal d'un paral.lelepípede: la diagonal del cos és combinació lineal de les arestes concurrents dels vèrtexs.

<iframe scrolling="no" title="Combinació lineal de vectors" src="https://www.geogebra.org/material/iframe/id/wbquxbzs/width/600/height/500/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="500px" style="border:0px;"> </iframe>


###Vectors linealment dependents i independents

Direm que un conjunt de vectors $\{\overrightarrow{ u }_1,\overrightarrow{ u }_2, \overrightarrow{ u }_3,...,\overrightarrow{ u }_n \}$ és __linealment dependent__ si com a mínim un dels vectors és combinació lineal dels altres.

Per exemple, el conjunt de vectors:

$$S=\{(3,3,2), (1,1,-1), (2,2,3)\}$$

és linealment dependent perquè:

$$(3,3,2)=1\cdot(1,1,-1)+1(2,2,3)$$

Si a un conjunt de vectors linalment dependents li afegim nous vectors, el conjunt resultant també serà linealment dependent. A la pràctica, que dos vectors siguin linealment dependents vol dir que són proporcionals i per tant tenen la mateixa direcció.

Direm que un conjunt de vectors $\{\overrightarrow{ u }_1,\overrightarrow{ u }_2, \overrightarrow{ u }_3,...,\overrightarrow{ u }_n \}$ és __linealment independent__ si cap dels vectors és combinació lineal dels altres.

Per saber si un conjunt de vectors donats és linealment independent només caldrà veure que al plantejar una combinació lineal entre ells, necessàriament perquè es compleixi la igualtat tots els escalars han de ser zero:

> Un conjunt de vectors $\{\overrightarrow{ u }_1,\overrightarrow{ u }_2, \overrightarrow{ u }_3,...,\overrightarrow{ u }_n \}$ és linealment independent $\Leftrightarrow$ $\lambda _1{\overrightarrow{ u }_1+ \lambda_ 2 \overrightarrow{ u }_2+ \lambda_3 \overrightarrow{ u }_3 +...+\lambda _n \overrightarrow{ u }_n}=\overrightarrow{ 0 } \forall \lambda_ i =0$

Si alguna de les constants és diferent de zero, llavors el conjunt és linealment dependent.

__Exemple 1__

Digues si el conjunt de vectors següent és linealment independent.

$$\{(1,1,2),(-1,5,0),(1,3,2)\}$$

Anem a veure si existeix alguna combinació lineal de tots ells on almenys una constant sigui diferent de zero:

$$\lambda_1 (1,1,2)+\lambda _2 (-1,5,0)+\lambda _3(1,3,2)=(0,0,0)$$

Per solucionar aquesta equació cal resoldre el sistema:

$$\begin{cases} \lambda_1-\lambda_2+\lambda_3=0 \\ \lambda_1+5\lambda_2+3\lambda_3=0 \\ 2\lambda_1+2\lambda_3=0 \end{cases}$$

És un sistema homogeni. Tal com vam veure [al tema passat](http://mdosil.cat/mates2batcientific/temes/sistemes/#sistemes-homogenis), els sistemes homogenis sempre són compatibles. Ara només caldrà veure si és:

* __Compatible determinat__. En aquest cas la solució és trivial amb totes les constants zero. Llavors el conjunt de vectors serà __linealment independent__.

* __Compatible indeterminat__. Hi ha infinites solucions i algunes d'elles no són igual a zero. Això voldrà dir que algun vector és combinació lineal dels altres i per tant el conjunt de vectors és __linealment dependent__.

Anem a resoldre el sistema pel mètode de Gauss:

$$ \left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 0\\
  1 & 5 & 3 & 0\\
  2 & 0 & 2 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 0\\
  0 & 6 & 2 & 0\\
  0 & 2 & 0 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & 1 & -1 & 0\\
  0 & 2 & 6 & 0\\
  0 & 0 & 2 & 0
\end{array}
\right)
$$

El sistema és compatible determinat amb la solució trivial $\lambda_1=\lambda_2=\lambda_3=0$ per tant són vectors linealment independents.

Per acabar, es pot demostrar que:

* Dos vectors alineats són linealment dependents (són proporcionals)
* Dos vectors no alineats són linealment independents
* Tres vectors coplanaris (en el mateix pla) són linealment dependents, perquè siguin independents no han de formar part del mateix pla.


Hi ha una altra manera de veure si un conjunt de vectors és linealment dependent o independent:

* Si $\overrightarrow{ u }$ i $\overrightarrow{ v }$ són 2 vectors a $\mathbb{ R }^3$:
    * Si el rang de la matriu obtinguda al posar com a files les components dels 2 vectors és 1, llavors els vectors són proporcionals i per tant, linealment dependents.

    * Si el rang d'aquesta matriu és 2, els vectors no són proporcionals (tenen direccions diferents) i per tant són linealment independents.

* Si $\overrightarrow{ u }$, $\overrightarrow{ v }$ i $\overrightarrow{ w }$ són 3 vectors a $\mathbb{ R }^3$:

    * Si el __determinant__ de la matriu obtinguda al posar com a files les components dels 3 vectors és 0, voldrà dir que el rang de la matriu és més petit que 3, i per tant, com a mínim un dels vectors és combinació lineal dels altres 2, són linealment dependents. De fet, en aquest cas els vectors són coplanaris (estan dins el mateix pla).

    * Si el __determinant__ de la matriu obtinguda al posar com a files les components dels 3 vectors és diferent de zero, voldrà dir que el rang de la matriu és 3, i el conjunt de vectors és linealment independent.

###Bases d'un espai vectorial

Anem a definir què és una base d'un espai vectorial:

> Donats $n$ vectors $\overrightarrow{ u }_1,\overrightarrow{ u }_2,...,\overrightarrow{ u }_n,$ direm que són base d'un espai vectorial $E$ si compleixen les condicions següents:

>* Són linealment independents
>* Generen tot l'espai vectorial $E$: Qualsevol vector de $E$ es pot expressar com a combinació lineal de tots ells.

El nombre de vectors linealment independents necessaris per formar una base d'un espai vectorial s'anomena __dimensió__.

####Bases a $\mathbb{R}^3$

En l'espai $\mathbb{R}^3$ qualsevol conjunt de $3$ vectors que siguin __linealment independents__ formaran base. La base més utilitzada però és __la base canònica__ amb els 3 vectors unitaris i ortogonals entre ells:

\begin{align}
\overrightarrow{ i }&=(1,0,0)\\
\overrightarrow{ j }&=(0,1,0)\\
\overrightarrow{ k }&=(0,0,1)\\
\end{align}

<iframe scrolling="no" title="Base canònica a R3" src="https://www.geogebra.org/material/iframe/id/PK47TUVR/width/480/height/545/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="480px" height="545px" style="border:0px;"> </iframe>


__Exemple 2__

El conjunt de vectors $<(2,1,1),(-1,-2,0),(1,-1,1)>$ formen base?

Veure si formen base és el mateix que demostrar que són linealment independents, o sigui, que cap d'ells es pot expressar com a combinació lineal dels altres dos.

Tal com hem dit, la solució a l'equació:

$$a(2,1,1)+b(-1,-2,0)+c(1,-1,1)=(0,0,0)$$

haurà de ser $a=0$, $b=0$ i $c=0$ (solució trivial) en cas que formin base. Si trobem alguna solució amb paràmetres diferents de zero llavors podem afirmar que com a mínim un dels vectors és combinació lineal dels altres dos, i per tant, no formen base.

L'equació vectorial anterior dóna lloc al sistema homogeni:

$$\begin{cases} 2a-b+c=0 \\ a-2b-c=0 \\ a+c=0 \end{cases}$$

Resolem-lo pel mètode de Gauss (ja canviem l'ordre de la 1a i la 2a equació):

$$ \left(
\begin{array}{ccc|c}
  1 & -2 & -1 & 0\\
  2 & -1 & 1 & 0\\
  1 & 0 & 1 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & -2 & 1 & 0\\
  0 & 3 & 3 & 0\\
  0 & 2 & 2 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & -2 & -1 & 0\\
  0 & 1 & 1 & 0\\
  0 & 2 & 2 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & -2 & -1 & 0\\
  0 & 1 & 1 & 0\\
  0 & 0 & 0 & 0
\end{array}
\right)
$$

És un sistema compatible indeterminat. Tenim 2 equacions i 3 incògnites, per tant, hi ha infinites solucions pels paràmetres, i per això, segur que alguna tindrà els 3 paràmetres diferents de zero. Podem afirmar doncs, que els 3 vectors __no formen base__  ja que podem expressar un d'ells com a combinació lineal dels altres dos. Anem a veure-ho ara.

Acabem de resoldre el sistema:

$$\begin{cases} a-2b-c=0 \\ b+c=0  \end{cases}$$

Si fem que $c=\lambda, \lambda \in \mathbb{ R }$, llavors:

$$a=-\lambda, b=-\lambda, c=\lambda \forall \lambda \in \mathbb{R}$$

Si agafem el valor $\lambda=1$ llavors:

$$a=-1, b=-1, c=1$$

i la combinació lineal seria:

\begin{align}
-1(2,1,1)-1(-1,-2,0)+1(1,-1,1)&=(0,0,0)\\
-1(2,1,1)&=(-1,-2,0)-1(1,-1,1)+(0,0,0)\\
(2,1,1)&=-1(-1,-2,0)+1(1,-1,1)\\
\end{align}

####Components d'un vector en una base

Descomposar un vector en una base voldrà dir escriure el vector com a combinació lineal de la base. Els escalars obtinguts els anomenarem __components del vector en aquella base__. Es pot demostrar que donada una base, les components del vector en aquella base __són úniques__.



__Exemple 3__

Donat el vector de components $\overrightarrow{ v }=(9,6,-4)$ en la base canònica, troba les seves components en la base $<(2,3,0),(3,1,-2),(1,1,0)>$.

Podem expressar el vector donat com:

$$(9,6,-4)=9(1,0,0)+6(0,1,0)-4(0,0,1)$$

Anem a expressar-lo en la base donada. Això vol dir que hem de trobar uns escalars $a$, $b$ i $c$ que compleixin:

$$(9,6,4)=a(2,3,0)+b(3,1,-2)+c(1,1,0)$$

Això dóna lloc al sistema:

$$\begin{cases} 2a+3b+c=9 \\ 3a+b+c=6 \\ -2b=-4  \end{cases}$$

Que com que és esglaonat el podem solucionar tranquil.lament i trobem que:

$$a=1, b=2, c=1$$

Per tant, el vector $\overrightarrow{ v }$ té components $(1,2,1)$ en la base $<(2,3,0),(3,1,-2),(1,1,0)>$.

##Producte escalar

Considerem ara dos vectors qualssevol de $\mathbb{ R }^3$. Podem afirmar que amb 2 vectors aquests estaran en el mateix pla. Si anomenem els 2 vectors $\overrightarrow{ u }$ i $\overrightarrow{ v }$, definim el producte escalar com:

$$\bbox[5px,border:2px solid black]{\overrightarrow{ u }\cdot \overrightarrow{ v }=|\overrightarrow{ u }|\cdot |\overrightarrow{ v }|\cdot \cos (\alpha)}$$

on $\alpha$ és l'angle que formen els 2 vectors amb $\alpha \le 90$.

Recordem que el producte escalar de 2 vectors és un nombre real.

També es pot demostrar que, si $\overrightarrow{ u }=(u_1,u_2,u_3)$ i $\overrightarrow{ v }=(v_1,v_2,v_3)$, el producte escalar també es pot expressar en components com:

$$\bbox[5px,border:2px solid black]{\overrightarrow{ u }\cdot \overrightarrow{ v }=u_1\cdot v_1+u_2\cdot v_2+u_3\cdot v_3}$$

###Propietats del producte escalar

* Commutativa: $\overrightarrow{ u }\cdot \overrightarrow{ v }=\overrightarrow{ v }\cdot \overrightarrow{ u }$
* Associativa: $\overrightarrow{ u }\cdot (\overrightarrow{ v }\cdot \overrightarrow{ w })=(\overrightarrow{ u }\cdot \overrightarrow{ v })\cdot \overrightarrow{ w }$
* Distributiva respecte la suma: $\overrightarrow{ u }\cdot (\overrightarrow{ v } + \overrightarrow{ w })=\overrightarrow{ u }\cdot \overrightarrow{ v } + \overrightarrow{ u }\cdot \overrightarrow{ w }$

Recordem que el producte escalar de dos vectors ortogonals (perpendiculars) és zero, i el producte escalar de dos vectors paral.lels és màxim igual al producte de mòduls.

###Projecció d'un vector sobre un altre

Considerem els vectors del gràfic $\overrightarrow{ AB }$ i $\overrightarrow{ AC }$.

<iframe scrolling="no" title="Projecció d'un vector sobre un altre a R3" src="https://www.geogebra.org/material/iframe/id/Vb2kRbK8/width/600/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="719px" style="border:0px;"> </iframe>

Si calculem el seu producte escalar dels vectors $\overrightarrow{ AB }$ i $\overrightarrow{ AC }$ obtenim:

$$\overrightarrow{ AB }\cdot \overrightarrow{ AC }=|\overrightarrow{ AB }|\cdot |\overrightarrow{ AC }|\cdot \cos \alpha=|\overrightarrow{ AD }|\cdot |\overrightarrow{ AC }|$$

$|\overrightarrow{ AD }|$ és la __projecció del vector $\overrightarrow{ AB }$ en la direcció del vector $\overrightarrow{ AC }$__.

En general, definim la projecció d'un vector $\overrightarrow{ a }$ sobre un vector $\overrightarrow{ b }$ com:

$$proj(\overrightarrow{ a }_{\overrightarrow{ b }})=\frac{ |\overrightarrow{ a }\cdot \overrightarrow{ b }|}{ |\overrightarrow{ b }| }=|\overrightarrow{ a }\cdot \overrightarrow{ u }_{\overrightarrow{ b }}|$$

on $\overrightarrow{ u }_{\overrightarrow{ b }}$ és un vector unitari amb la mateixa direcció i sentit que $\overrightarrow{ b }$.

##Producte vectorial

Donats dos vectors $\overrightarrow{ u }=(u_1,u_2,u_3)$ i $\overrightarrow{ v }=(v_1,v_2,v_3)$, el producte vectorial d'aquests dos vectors és un vector $\overrightarrow{ w }=\overrightarrow{ u } \times \overrightarrow{ v }$ __perpendicular__ als vectors $\overrightarrow{ u }$ i $\overrightarrow{ v }$.


<iframe scrolling="no" title="producte vectorial entre 2 vectors" src="https://www.geogebra.org/material/iframe/id/nQcGYyDP/width/900/height/692/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="900px" height="692px" style="border:0px;"> </iframe>

Es pot demostrar que els components del vector producte vectorial es troben calculant el determinant següent:

$$
\overrightarrow{ u } \times \overrightarrow{ v }=
\begin{vmatrix}
\overrightarrow{ i } & \overrightarrow{ j } & \overrightarrow{ k } \\
u_1 & u_2 & u_3\\
v_1 & v_2 & v_3
\end{vmatrix}
$$

on $\overrightarrow{ i }=(1,0,0)$, $\overrightarrow{ j }=(0,1,0)$ i $\overrightarrow{ k }=(0,0,1)$.

###Propietats del producte vectorial

1. El mòdul del producte vectorial es calcula segons: $|\overrightarrow{ u } \times \overrightarrow{ v }|=|\overrightarrow{ u }|\cdot |\overrightarrow{ v }|\cdot \sin(\overrightarrow{ u },\overrightarrow{ v })$
2. El producte vectorial és anticommutatiu: $\overrightarrow{ u } \times \overrightarrow{ v }=-\overrightarrow{ v } \times \overrightarrow{ u }$
3. Associativa respecte el producte per un escalar: $k\cdot (\overrightarrow{ u } \times \overrightarrow{ v })= (k\cdot \overrightarrow{ u }) \times \overrightarrow{ v }$
4. Distributiva respecte la suma: $\overrightarrow{ u } \times (\overrightarrow{ v } + \overrightarrow{ w })= \overrightarrow{ u } \times \overrightarrow{ v } +\overrightarrow{ u } \times \overrightarrow{ w }$



##Producte mixt

Donats 3 vectors $\overrightarrow{ u }=(u_1,u_2,u_3)$, $\overrightarrow{ v }=(v_1,v_2,v_3)$ i $\overrightarrow{ w }=(w_1,w_2,w_3)$ definim el __producte mixt__ com:

$$\overrightarrow{ u }\cdot (\overrightarrow{ v }\times \overrightarrow{ w })$$

Es pot demostrar que el resultat de fer aquesta operació s'obté resolent el determinant següent:

$$
\overrightarrow{ u }\cdot (\overrightarrow{ v } \times \overrightarrow{ w })=
\begin{vmatrix}
u_1 & u_2 & u_3 \\
v_1 & v_2 & v_3\\
w_1 & w_2 & w_3
\end{vmatrix}
$$

Ja veiem que el producte mixt dóna lloc a un nombre real.



##Aplicacions

###Càlcul de l'àrea d'un paral.lelogram

Imagineu que volem calcular l'àrea del paral.lelogram de la figura:

<iframe scrolling="no" title="Àrea paral.lelogram" src="https://www.geogebra.org/material/iframe/id/EXurDN2J/width/600/height/529/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="529px" style="border:0px;"> </iframe>

L'àrea d'un paral.lelogram $A_p$ és la seva base multiplicada per l'altura. En el dibuix:

\begin{align}
A_p&=|\overrightarrow{ u }|\cdot h\\
h&=|\overrightarrow{ v }|\cdot \sin \alpha\\
A_p&=|\overrightarrow{ u }|\cdot |\overrightarrow{ v }|\cdot \sin \alpha\\
A_p&=|\overrightarrow{ u }\times \overrightarrow{ v }|
\end{align}

Per tant, l'àrea d'un paral.lelogram és el mòdul del producte vectorial dels vectors base i lateral.

###Càlcul del volum d'un paral.lelepípede

Considerem el paral.lelepípede de la figura:

<iframe scrolling="no" title="paral.lelepípede" src="https://www.geogebra.org/material/iframe/id/WsH8zBcP/width/900/height/505/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="900px" height="505px" style="border:0px;"> </iframe>

Per calcular el seu volum, hem de trobar l'àrea de la base (que ja l'hem trobada a l'apartat anterior) i multiplicar-ho per l'altura, $h$. Si ens hi fixem, l'altura és la projecció ortogonal del vector $\overrightarrow{ a }$ en la direcció perpendicular a la base, o sigui, el pla determinat pels vectors $\overrightarrow{ b }$ i $\overrightarrow{ c }$:

$$h=\overrightarrow{ a }\cdot \frac{ \overrightarrow{ b }\times \overrightarrow{ c }}{ |\overrightarrow{ b }\times \overrightarrow{ c }| }$$

Per tant, el volum és:

$$V=|\overrightarrow{ b }\times \overrightarrow{ c }|\cdot h=|\overrightarrow{ b }\times \overrightarrow{ c }|\cdot \overrightarrow{ a }\cdot \frac{ \overrightarrow{ b }\times \overrightarrow{ c }}{ |\overrightarrow{ b }\times \overrightarrow{ c }| }=|\overrightarrow{ a }\cdot (\overrightarrow{ b }\times \overrightarrow{ c })|$$

El volum és el producte mixt entre els vectors $\overrightarrow{ a }, \overrightarrow{ b }, \overrightarrow{ c }$.

###Moviment d'una partícula carregada dins d'un camp magnètic

En física, quan una partícula carregada viatja a través d'un cap elèctric $\overrightarrow{ E }$ i un camp magnètic $\overrightarrow{ B }$, aquesta experimenta una força anomenada [Força de Lorentz](https://en.wikipedia.org/wiki/Lorentz_force) segons:

$$\overrightarrow{ F }=q\cdot \overrightarrow{ E }+q\cdot \overrightarrow{ v }\times \overrightarrow{ B }$$

on $q$ és la càrrega de la partícula i $\overrightarrow{ v }$ la seva velocitat. Si estudiem una mica la fòrmula veiem que gaudeix de dues parts. Una primera part deguda a la intensitat de camp elèctric $\overrightarrow{ E }$ que propulsa la partícula en la mateixa direcció que el seu moviment, i una segona part deguda al camp magnètic $\overrightarrow{ B }$ que impulsa la partícula amb una força perpendicular a la seva velocitat (per la naturalesa del producte vectorial).

Ens fixarem en aquesta segona part, $\overrightarrow{ F }_m=q\cdot \overrightarrow{ v }\times \overrightarrow{ B }$. Si calculem el mòdul del producte vectorial obtenim:

$$|\overrightarrow{ F }_m|=|q|\cdot| \overrightarrow{ v }\times \overrightarrow{ B }|=q\cdot v \cdot B \sin \theta$$

on $\theta$ és l'angle entre la velocitat de desplaçament de la partícula $\overrightarrow{ v }$ i el camp magnètic \overrightarrow{ B }. D'aquesta manera, quan la velocitat i el camp magnètic són paral.lels, aquesta part de la força es cancel.la, i la partícula segueix la mateixa trajectòria, paral.lela al camp elèctric. Però si no són paral.lels, la partícula comença a experimentar una força perpendicular a la seva direcció de moviment, fet que fa que la partícula experimenti una trajectòria circular. En absència de camp elèctric, Si $\overrightarrow{ v }$ i \overrightarrow{ B } són perpendiculars, la trajectòria de la partícula serà circular, i si l'angle entre el camp magnètic i la velocitat està entre zero i noranta graus, $0<\theta<90$, la trajectòria de la partícula serà helicoidal. Cliqueu [aquest enllaç](https://courses.lumenlearning.com/boundless-physics/chapter/motion-of-a-charged-particle-in-a-magnetic-field/) per una explicació més detallada del fenomen.

Aquest fet va ser aprofitat per dissenyar els primers detectors de partícules subatòmiques al [CERN](www.cerh.ch), [les càmeres de bombolles](https://courses.lumenlearning.com/boundless-physics/chapter/motion-of-a-charged-particle-in-a-magnetic-field/). Les partícules carregades, producte de desintegracions atòmiques, atravessaven un medi aquós i en presència d'un camp magnètic, experimentaven trajectòries helicoidals. La mesura el radi d'aquestes trajectòries permetia trobar les velocitats originals de les partícules.

![Trajectòries helicoidals de partícules carregades atravessant un medi d'hidrogen-neó líquid (Font: CERN)](img/bubble-chamber-bebc.jpg)

*Trajectòries helicoidals de partícules carregades atravessant un medi d'hidrogen-neó líquid (Font: CERN)*
