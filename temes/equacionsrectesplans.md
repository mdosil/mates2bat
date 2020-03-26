#Tema 8: Rectes i plans

##La Recta. Equacions

Tal com vèiem [al curs passat](http://mdosil.cat/mates1batcientific/temes/rectes/#equacio-vectorial), per determinar una recta ens fa falta un punt que hi pertanyi i un *vector director*, que és aquell que té la mateixa direcció que la recta. Ara només cal interpretar aquesta informació en tres dimensions enlloc de dues.

<iframe scrolling="no" title="Recta a R3" src="https://www.geogebra.org/material/iframe/id/yWW2AeBB/width/600/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="719px" style="border:0px;"> </iframe>

1. __Equació vectorial__

    Donat un punt qualsevol $P=(a,b,c)$ d'una recta $r$, i un vector director d'aquesta recta, $\overrightarrow{ u }=(u_1,u_2,u_3)$, podem afirmar que un punt $X=(x,y,z)$ pertany a la recta $r$ si el podem obtenir a partir de sumar al punt $P$ un determinat nombre de vegades ($\lambda$, $\lambda \in \mathbb{ R }$) la direcció del vector $\overrightarrow{ u }$:

    $$\bbox[5px,border:2px solid black]{(x,y,z)=(a,b,c)+\lambda (u_1,u_2,u_3)}$$

2. __Equacions paramètriques__

    Si igualem component a component l'equació anterior obtenim les equacions paramètriques de la recta:

    $$
    \bbox[5px,border:2px solid black]{\begin{cases} x=a+\lambda u_1 \\ y=b+\lambda u_2 \\ z=c+\lambda u_3 \end{cases} }
    $$

3. __Equació contínua__

    Si aïllem la $\lambda$ de les equacions anteriors, obtenim l'equació contínua de la recta:

    $$\bbox[5px,border:2px solid black]{\frac{ x-a }{ u_1 }=\frac{ y-b }{ u_2 }=\frac{ z-c }{ u_3 }}$$

4. __Equació implícita o cartesiana__

    Finalment, si agrupem les equacions anteriors dos a dos, obtindrem un sistema de 3 equacions i 3 incògnites compatible indeterminat (ho haurà de ser perquè la recta té només 2 dimensions, per tant, alguna de les equacions haurà de ser combinació lineal de les altres dues). Això vol dir que podem prescindir d'una de les equacions. I si anomenem $A, A^{\prime}$, $B, B^{\prime}$, $C, C^{\prime}$, els coeficients de les variables $x$, $y$ i $z$ respectivament, i $D, D^{\prime}$ els termes independents, podem reescriure les equacions anteriors com:

    $$
    \bbox[5px,border:2px solid black]{\begin{cases} Ax+By+Cz+D&=0 \\ A^{\prime}x+B^{\prime}y+C^{\prime}z+D^{\prime}&=0  \end{cases} }
    $$


__Exemple 1__

Dóna l'equació de la recta que passa pel punt $P=(2,1,0)$ i és paral.lela a la recta d'equació paramètrica:

$$
\begin{cases} x=3+\lambda  \\ y=2+2 \lambda \\ z= 3 - \lambda  \end{cases}
$$

Si és paral.lela a aquesta recta, tindrà el mateix vector director: $\overrightarrow{ u }=(1,2,-1)$. Si tenim el punt i el vector, podem donar aquesta recta utilitzant l'equació contínua:

$$\frac{ x-2 }{ 1 }=\frac{ y-1 }{ 2 }=\frac{ z-0 }{ -1 }$$

###Equacions dels eixos de coordenades

Els eixos de coordenades ($x$, $y$ i $z$) tenen vectors directors (base canònica) $\overrightarrow{ i }=(1,0,0)$, $\overrightarrow{ j }=(0,1,0)$ i $\overrightarrow{ k }=(0,0,1)$ respectivament. Si prenem les equacions paramètriques de la recta i aquests vectors obtenim:

| Eix x   |    Eix y     |  Eix z |
|:----------|:--------------|:-------|
| $\begin{cases} x=\lambda \\ y=0 \\ z=0 \end{cases}$ |\begin{cases} x=0 \\ y=\lambda \\ z=0 \end{cases}|\begin{cases} x=0\\ y=0 \\ z=\lambda \end{cases}|


##El Pla. Equacions

Si per definir una recta necessitàvem una direcció (vector) i un punt de la recta, per a definir un pla necessitarem 3 elements: un punt $P=(a,b,c)$ del pla, i un parell de vectors $\overrightarrow{ u }=(u_1,u_2,u_3)$ i $\overrightarrow{ v }=(v_1,v_2,v_3)$ linealment independents que es trobin dins del pla. A partir d'aquí, qualsevol punt del pla $X=(x,y,z)$ es podrà trobar sumant al punt $P$ una combinació lineal dels 2 vectors.

<iframe scrolling="no" title="Pla a R3" src="https://www.geogebra.org/material/iframe/id/zMY3SeJ9/width/600/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="600px" height="719px" style="border:0px;"> </iframe>

1. __Equació vectorial__

    Si escrivim el que hem dit al paràgraf anterior de manera algebraica obtenim:

    $$X=P+\alpha \overrightarrow{ u }+ \beta \overrightarrow{ v }$$

    on $\alpha$ i $\beta$ són nombres reals.

    Escrit en components, obtenim l'equació vectorial del pla:

    $$\bbox[5px,border:2px solid black]{(x,y,z)=(a,b,c)+\alpha (u_1,u_2,u_3)+\beta (v_1,v_2,v_3)}$$

2. __Equacions paramètriques__

    Si escrivim l'equació vectorial del pla component a component obtenim les seves equacions paramètriques:

    $$
    \bbox[5px,border:2px solid black]{\begin{cases} x=a+\alpha u_1 +\beta v_1 \\ y=b+\alpha u_2+ \beta v_2 \\ z=c+\alpha u_3 + \beta v_3 \end{cases} }
    $$
3. __Equació general, implícita o cartesiana__

    Hi ha diverses maneres d'arribar a aquesta equació. Si pensem en la primera equació que hem escrit (vectorial) i passem el punt $P$ restant a la banda esquerra de l'equació obtenim:

    $$X-P=\alpha \overrightarrow{ u }+ \beta \overrightarrow{ v }$$

    que dit d'una altra manera significa que el vector $\overrightarrow{ PX }$ és combinació lineal dels vectors $\overrightarrow{ u }$ i $\overrightarrow{ v }$. Com que $\overrightarrow{ u }$ i $\overrightarrow{ v }$ són linealment independents per construcció, això és el mateix que dir que el rang de la matriu formada per les components dels vectors $\overrightarrow{ PX }$, $\overrightarrow{ u }$ i $\overrightarrow{ v }$ ha de ser necessàriament 2, i per tant, el determinant d'aquesta matriu ha de ser zero:

    $$Det(\overrightarrow{ PX }, \overrightarrow{ u }, \overrightarrow{ v })=\begin{vmatrix}
    x-a & u_1 & v_1 \\
    y-b & u_2 & v_2\\
    z-c & u_3 & v_3
    \end{vmatrix}=0
    $$

    Agrupant termes i assignant les lletres $A$, $B$, $C$ als coeficients de les variables i $D$ pel terme independent obtenim:

    $$\bbox[5px,border:2px solid black]{Ax+By+Cz+D=0}$$

__Exemple 2__

Donats 3 punts: $A=(-1,2,3)$, $B=(0,1,-3)$ i $C=(1,1,1)$. Estan alineats? En cas contrari, determina l'equació general del pla que els conté.

Per veure si els 3 punts estan alineats només caldrà buscar 2 vectors determinats per aquests 3 punts i veure si són linealment dependents:



$$\begin{cases}  \overrightarrow{ AB }=(1,-1,-6) \\ \overrightarrow{ AC }=(2,-1,2)  \end{cases}\rightarrow \frac{ 1 }{ 2 } \ne \frac{ -1 }{ -1 } \ne \frac{ -6 }{ 2 }$$

Per tant, els 2 vectors són linealment independents. Això vol dir que els 3 punts no estan alineats i formen triangle i per tant, estan en un mateix pla.

Per trobar l'equació d'aquest pla només cal que exigim que, donat un punt qualsevol del pla $X=(x,y,z)$ els vectors  $\overrightarrow{ AX }$, $\overrightarrow{ AB }$ i $\overrightarrow{ AC }$ siguin linealment dependents, que és el mateix que exigir que el determinant dels vectors posats en columnes sigui zero:

$$\begin{vmatrix}
x+1 & 1 & 2 \\
y-2 & -1 & -1\\
z-3 & -6 & -2
\end{vmatrix}=0\rightarrow 4x+10y-z-13=0
$$

###Vector normal associat a un pla

Es pot demostrar amb els coeficients de les variables que defineixen l'equació d'un pla obtenim un vector normal (perpendicular) a aquest pla. Per tant, podem afirmar que un pla d'equació $Ax+By+Cz+D=0$ té sempre un vector perpendicular a aquest de components:

$$\overrightarrow{ n }=(A,B,C)$$

###Equacions dels plans $xy$, $zy$ i $xz$

Les equacions d'aquests plans són molt senzilles:

| Pla $xy$ | Pla $zy$     | Pla $xz$ |
| :-------| :---------- |:--------|
| $z=0$    | $x=0$        | $y=0$    |

###Punts coplanaris

Donats 3 punts de $\mathbb{ R }^3$ aquests sempre seran coplanaris. En cas de tenir-ne més, caldrà comprovar si existeix un pla que els contingui a tots.

__Exemple 3__

Determina si els punts $A=(2,3,0)$, $B(4,5,-1)$, $C=(3,2,3)$ i $D=(0,-1,-2)$ són coplanaris.

El que farem és trobar l'equació del pla que conté els 3 primers punts i mirarem si el quart punt hi pertany. Per trobar l'equació del pla, utilitzem el procediment explicat anteriorment per trobar l'equació general del pla. Calculem els vectors:

$$\overrightarrow{ AB }=(2,2,-1)\qquad \overrightarrow{ AC }=(1,-1,3)$$

Donat un punt qualsevol del pla $X=(x,y,z)$, els vectors $\overrightarrow{ AX }$, $\overrightarrow{ AB }$ i $\overrightarrow{ AC }$ seran coplanaris si són linealment dependents, o el que és el mateix, el seu determinant és zero:

$$\begin{vmatrix}
x-2 & 2 & 1 \\
y-3 & 2 & -1\\
z & -1 & 3
\end{vmatrix}=0\rightarrow 5x-7y-4z+11=0
$$

Aquesta és l'equació del pla que conté els 3 primers punts. Ara, per saber si el quart punt pertany al pla, només cal substituir les coordenades de $D$ en l'equació d'aquest i veure si la compleix:

$$5\cdot 0-7\cdot (-1)-4\cdot(-2)+11\ne 0$$

Com que no compleix l'equació del pla, podem afirmar que els 4 punts no són coplanaris.

###Vectors coplanaris

Per veure si un conjunt de 3 o més vectors són coplanaris només hem de veure si tots els menors d'ordre 3 són zero. Dit d'una altra manera, exigim que la dimensió no sigui 3, sinó que com a màxim pot ser 2 i per tant, pertanyen al mateix pla.

__Exemple 4__

Determina si els vectors $\overrightarrow{ u }=(0,3,5)$, $\overrightarrow{ v }=(1,2,2)$ i $\overrightarrow{ w }=(-1,0,3)$ són coplanaris.

Anem a calcular el determinant:

$$\begin{vmatrix}
0 & 1 & -1 \\
3 & 2 & 0\\
5 & 2 & 3
\end{vmatrix}=-5
$$

Els 3 vectors són linealment independents, per tant, no estan sobre el mateix pla.

###Rectes coplanàries

Per comprovar si 2 rectes són complanàries, caldrà veure si els seus vectors directors juntament amb un tercer punt obtingut de dos punts (un de cada recta) són linealment dependents. En cas afirmatiu, són coplanàries, i en cas contrari, no.

__Exemple 5__

Determina si les rectes $r \equiv \begin{cases} x=1+2 \lambda \\ y=3 \lambda \\ z=5- \lambda \end{cases}$ i $s \equiv \frac{ x-1 }{ 5 }=\frac{ y-3 }{ 1 }=\frac{ z + 2 }{ 2 }$ són coplanàries.

De la recta $r$ en trobem el seu vector director $\overrightarrow{ u }=(2,3,-1)$ i un punt $A=(1,0,5)$. Fem el mateix per la recta $s$: $\overrightarrow{ v }=(5,1,2)$ i $B=(1,3,-2)$. Construïm un tercer vector $\overrightarrow{ AB }=(0,3,-7)$. El que ens cal ara és mirar si els 3 vectors són linealment dependents (determinant igual a zero). En cas afirmatiu les rectes seran coplanàries.


$$\begin{vmatrix}
0 & 2 & 5 \\
3 & 3 & 1\\
-7 & -1 & 2
\end{vmatrix}=64
$$

Els 3 vectors són linealment independents. Per tant, les dues rectes no són coplanàries.


##Posició relativa de dues rectes

### Considerant els vectors directors

Donades dues rectes a l'espai $r$ i $s$, amb vectors directors $\overrightarrow{ u }$ i $\overrightarrow{ v }$ respectivament, ens podem trobar amb 4 situacions diferents:

1. __Rectes coincidents__

    Els vectors directors són iguals o proporcionals i agafant un punt qualsevol de la primera recta comprovem que també compleix l'equació de la segona recta.

2. __Rectes paral.leles no coincidents__

    Els vectors directors són iguals o proporcionals però agafant un punt qualsevol de la primera recta comprovem que no compleix l'equació de la segona recta.

3. __Rectes secants__

    Els vectors directors no són paral.lels. El determinant resultant de posar en columnes el vector $\overrightarrow{ u }$, $\overrightarrow{ v }$ i un tercer vector format per 2 punts (un de cada recta) és $0$ (el rang de la matriu és 2 i per tant, les dues rectes són coplanàries i es tallen).

4. __Rectes que es creuen__

    Els vectors directors no són paral.lels. El determinant resultant de posar en columnes el vector $\overrightarrow{ u }$, $\overrightarrow{ v }$ i un tercer vector format per 2 punts (un de cada recta) és diferent de $0$ (el rang de la matriu és 3 i per tant, les dues rectes es troben en plans diferents i no es tallen).

5. __Rectes perpendiculars__

    El producte escalar dels seus vectors és zero: $\overrightarrow{ u }\cdot \overrightarrow{ v }=0$. Aquestes dues rectes no tenen perquè tallar-se. Són un cas particular de l'apartat 3 o de l'apartat 4.

###Considerant les seves equacions implícites

També podem considerar la posició relativa de dues rectes agafant les equacions implícites de cadascuna. En aquest cas, obtindrem un sistema de $4$ equacions i $3$ incògnites que haurem de solucionar. Ens podem trobar en 4 casos diferents:

1. __Sistema compatible determinat__

    Té una única solució. Aquesta solució són les coordenades $(x,y,z)$ del punt de tall de les dues rectes. Les rectes són secants.

2. __Sistema incompatible__

    No té solució. En aquest cas les rectes poden creuar-se o ser paral.leles. Caldrà comprovar si els vectors directors de cadascuna de les rectes són proporcionals o no per determinar-ne cada cas.

3. __Sistema compatible indeterminat__

    Té infinites solucions. Les rectes són coincidents.

__Exemple 6__

Troba la posició relativa de les rectes:

$$r \equiv \begin{cases}  x=3+\lambda \\ y=2+2 \lambda \\ z=3-\lambda  \end{cases} \qquad s \equiv \begin{cases}  3x+z=0 \\ 2x+y=-1  \end{cases}$$

El problema es pot resoldre de moltes maneres. El que farem primer és expressar $r$ també de forma implícita:

$$\frac{ x-3 }{ 1 }=\frac{ y-2 }{ 2 }=\frac{ z -3 }{ -1 }\rightarrow r\equiv \begin{cases}  2x-y=4 \\ y+2z=8 \end{cases} $$

Agafem les 4 equacions de les dues rectes i resolem el sistema 4$\times$3 (4 equacions i 3 incògnites):


$$\begin{cases}  3x+z=0\\ 2x+y=-1 \\ 2x-y=4 \\ y+2z=8  \end{cases} $$

Si utilitzem [el mètode de Gauss](http://mdosil.cat/mates2batcientific/temes/sistemes/#metode-de-gauss):


$$ \left(
\begin{array}{ccc|c}
  3 & 0 & 1 & 0\\
  2 & 1 & 0 & -1\\
  2 & -1 & 0 & 4\\
  0 & 1 & 2 & 8
\end{array}
\right)
=\left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  2 & 1 & 0 & -1\\
  2 & -1 & 0 & 4\\
  0 & 1 & 2 & 8
\end{array}
\right)
=\left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  0 & 3 & -2 & -3\\
  0 & 1 & -2 & 2\\
  0 & 1 & 2 & 8
\end{array}
\right)
=\left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  0 & 1 & -2 & 2\\
  0 & 3 & -2 & -3\\
  0 & 1 & 2 & 8
\end{array}
\right)
=\left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  0 & 1 & -2 & 2\\
  0 & 0 & 4 & -9\\
  0 & 0 & 4 & 6
\end{array}
\right)
$$

Veiem que el sistema és incompatible. Les rectes o bé són paral.leles o es creuen. Per veure en quin dels casos ens trobem, caldrà veure els vectors directors (que podem deduir de les equacions del principi). En el cas de $r$ el vector director és immediat: $\overrightarrow{ u }=(1,2,-1)$. Pel que fa a la recta $s$, per trobar el vector director caldrà transformar l'equació implícita en contínua. Per fer-ho aïllem la $x$ de les dues equacions i igualem:

$$x=\frac{ y+1 }{ -2 }=\frac{ z }{ -3 }$$

Per tant, el vector director de la recta $s$ és: $\overrightarrow{ v }=(1,-2,-3)$. Veiem que els 2 vectors no són proporcionals. Per tant, les rectes es creuen.




###Angle entre dues rectes

Per trobar l'angle entre dues rectes només caldrà trobar els seus vectors directors i aplicar la fòrmula del producte escalar. Si $r$ i $s$ són dues rectes de vectors directors $\overrightarrow{ u }$ i $\overrightarrow{ v }$ respectivament, l'angle $\alpha$ entre les dues rectes ($0 \le \alpha \le 90$) serà:

$$\alpha= arccos \frac{ |\overrightarrow{ u }\cdot \overrightarrow{ v }| }{ |\overrightarrow{ u }|\cdot |\overrightarrow{ v }| }$$


##Posició relativa entre rectes i plans

Donat un pla i una recta ens podem trobar amb 3 casos diferents:

1. __La recta i el pla són paral.lels__

    El producte escalar entre el vector director de la recta i el vector normal al pla és zero. Això vol dir que els 2 vectors són perpendiculars i per tant, el pla i la recta són paral.lels. Si agafem un punt de la recta i el substituïm a l'equació del pla i aquest no compleix l'equació del pla, ens trobarem en aquest cas. Si la compleix, estarem en el cas següent.

    Una altra manera de comprovar-ho és fent un sistema $3\times 3$ amb les dues equacions implícites de la recta i l'equació general del pla. Trobarem que el sistema és __incompatible__.

2. __La recta pertany al pla__

    Es pot comprovar com l'apartat anterior. En cas de decidir resoldre el sistema d'equacions, trobarem que el sistema és __compatible indeterminat__.

3. __La recta i el pla són secants__

    El producte escalar del vector normal al pla i del vector director de la recta no és zero. Per trobar el punt d'intersecció cal resoldre el sistema esmentat anteriorment. El sistema és __compatible determinat__ i la solució és el punt de tall.

__Exemple 7__

Determina la posició relativa entre la recta $r \equiv \frac{ x-1 }{ 2 }=\frac{ y-2 }{ 3 }=\frac{ z-3 }{ 4 }$ i el pla $\pi \equiv  4x+5y-2z+7=0$.

Podríem expressar la recta $r$ de forma implícita i resoldre el sistema d'equacions. Però una manera més ràpida és expressar la recta de forma paramètrica i substituir els valors de $x$, $y$ i $z$ en l'equació del pla i aïllar el paràmetre $\lambda$. En cas de trobar-lo, aquest és el punt de tall. Si arribem a una identitat ($0=0$) la recta està continguda en el pla. I si arribem a una igualtat no certa, recta i pla són paral.lels.

La recta $r$ per tant és:

$$r \equiv \begin{cases}  x=1+2\lambda \\ y=2+3 \lambda \\ z=3+4\lambda  \end{cases}$$

Si substituïm això a l'equació del pla obtenim:

$$4(1+2\lambda)+5(2+3\lambda)-2(3+4\lambda)+7=0\rightarrow \lambda=-1$$

Per tant, el punt de tall serà:

$$x=-1\qquad y=-1 \qquad z=-1$$



###Angle entre recta i pla

Volem calcular l'angle $\beta$ entre una recta i un pla qualsevol. Ens guiarem però amb el gràfic del cas particular en que la recta talla el pla:

<iframe scrolling="no" title="Angle entre recta i pla" src="https://www.geogebra.org/material/iframe/id/Kc63DEum/width/701/height/502/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="701px" height="502px" style="border:0px;"> </iframe>

Veiem que els angles $\alpha$ i $\beta$ són complementaris, això vol dir que  [es compleix](http://mdosil.cat/mates1batcientific/temes/trigonometria/#raons-trigonometriques-dangles-complementaris): $\sin(\beta)=\cos(\alpha)$ i viceversa.

Per tant, puc obtenir $\cos(\alpha)$ a partir del producte escalar de $\overrightarrow{ n }$ i $\overrightarrow{ u }$ i aquest igualar aquesta quantitat al $\sin(\beta)$:

$$\sin(\beta)=\cos(\alpha)=\frac{ |\overrightarrow{ n }\cdot {\overrightarrow{ u }}| }{ |\overrightarrow{ n }|\cdot |\overrightarrow{ u }|}$$

Recordem que fem el valor absolut del producte escalar perquè s'agafa com a angle entre recta i pla l'angle més petit que formen els dos ($\le 90$).

__Exemple 8__

Calcula l'angle entre la recta $r\equiv \frac{ x-1 }{ 2 }=\frac{y-2}{3}=\frac{ z-3 }{ 4 }$ i el pla $\pi\equiv 4x+5y-2z+7=0$

Amb les dades que ens donen tenim que: $\overrightarrow{ u }=(2,3,4)$ és el vector director de la recta i $\overrightarrow{ n }=(4,5,-2)$ el vector normal al pla. Aplicant la fòrmula tenim:

$$\sin \alpha=\frac{ |8+15-8| }{ \sqrt{4+9+16}\cdot \sqrt{ 16+25+4 }}=...\simeq 0.4152\rightarrow \alpha= 24^0 32^\prime$$

##Posició relativa entre plans

###Posició relativa de dos plans

Donats dos plans: $\pi_1 \equiv A_1x+B_1y+C_1z+D_1=0$ i $\pi_2 \equiv A_2x+B_2y+C_2z+D_2=0$, ens podem trobar amb 3 casos diferents:

1. __Plans paral.lels i coincidents__

    En aquest cas els vectors directors seran proporcionals, i en conseqüència, els vectors normals dels plans també. A més a més, l'equació del pla és la mateixa (o la mateixa multiplicada per un nombre). Per tant, es complirà:

    $$\frac{ A_1 }{ A_2 }=\frac{ B_1 }{ B_2 }=\frac{ C_1 }{ C_2 }=\frac{ D_1 }{ D_2 }$$


2. __Plans paral.lels i no coincidents__

    En aquest cas els vectors directors (i els vectors normals) seran proporcionals, però les dues equacions no són iguals. Per tant tindrem que:


    $$\frac{ A_1 }{ A_2 }=\frac{ B_1 }{ B_2 }=\frac{ C_1 }{ C_2 }\neq\frac{ D_1 }{ D_2 }$$



3. __Plans secants__

     En aquest cas no es compliran cap de les condicions anteriors. Però podem distingir 2 casos, depenent si el producte escalar de vectors normals és zero o no:

     1. __Plans secants no perpendiculars__: $ A_1\cdot A_2+B_1\cdot B_2+C_1\cdot C_2 \neq 0$

     2. __Plans secants i perpendiculars__: $ A_1\cdot A_2+B_1\cdot B_2+C_1\cdot C_2 = 0$



__Exemple 9__

Doneu l'equació del pla paral.lel al pla $\pi \equiv x-y-2z=0$ que passa per l'origen de coordenades.

En aquest cas, el pla tindrà la forma:

$$x-y-2z+D=0$$

Per trobar $D$ només cal que substituïm les coordenades de l'origen a l'equació del pla. Amb això obtenim: $D=0$. Per tant, l'equació del pla és:

$$x-y-2z=0$$

###Posició relativa de 3 plans

Si l'equació general de 3 plans, obtenim un sistema $3\times 3$. Per saber-ne la posició relativa només ens caldrà recordar el que vam aprendre sobre [el tipus de sistemes](http://mdosil.cat/mates2batcientific/temes/sistemes/#metode-de-resolucio-general-de-sistemes) estudiant el rang de la matriu de coeficients, $A$ i de la matriu ampliada, $MA$:

1. $Rang A=Rang MA=3\rightarrow$ El sistema és compatible determinat i té una única solució, els plans es tallen en un punt.
2. $Rang A=Rang MA=2\rightarrow$ El sistema és compatible indeterminat i té infinites solucions, els plans es tallen en una recta.
3. $Rang A \neq Rang MA\rightarrow$ El sistema és incompatible i no té solució, els plans no es tallen. Aquí poden passar vàries possibilitats, per exemple que siguin paral.lels, que es tallin dos a dos...

__Exemple 10__

Determina la posició dels següents plans en funció del paràmetre $a$:

$$\pi_1: x+y+az=1 \qquad \pi_2: 2x+ay=1 \qquad \pi_3: ax+y+z=1 \qquad$$


Si escrivim la matriu de coeficients $A$ i la matriu ampliada, $MA$, tenim que:

$$ A=\left(
\begin{array}{ccc}
  1 & 1 & a\\
  2 & a & 0\\
  a & 1 & 1
\end{array}
\right)
\qquad
\left(
\begin{array}{ccc|c}
  1 & 1 & a & 1\\
  2 & a & 0 & 1\\
  a & 1 & 1 & 1
\end{array}
\right)
$$

Calculem ara el determinant de la matriu $A$:

$$
|A|=-a^3+3a-2=-(a-1)^2(a+2)
$$

Si l'igualem a zero, veiem que s'anul.la pels valors $a=-2$ i $a=1$. Per tant, podem definir 2 casos:

1. Si $a \neq -2$ i $a \neq 1$:

    Ens trobem que Rang $A=$ Rang $MA=3$. Per tant el sistema és compatible determinant i els 3 plans es tallen en un punt.

2. Si $a=-2$:

    $$ A=\left(
    \begin{array}{ccc}
     1 & 1 & -2\\
     2 & -2 & 0\\
     -2 & 1 & 1
    \end{array}
    \right)
    \qquad
    \left(
    \begin{array}{ccc|c}
    1 & 1 & -2 & 1\\
    2 & -2 & 0 & 1\\
    -2 & 1 & 1 & 1
    \end{array}
    \right)
    $$

    Si orlem el menor d'ordre 2 amb el vector columna dels termes independents de la matriu ampliada obtenim que:

    $$\begin{vmatrix}
    1 & 1 & 1 \\
    2 & -2 & 1\\
    -2 & 1 & 1
    \end{vmatrix}=-9
    $$

    Per tant, en aquest cas, Rang $A=2$, Rang $MA=3$. Com que no coincideixen el sistema és incompatible i els plans no es tallen. Per veure la seva posició relativa, mirem els coeficients dels plans i veiem que no són proporcionals. Aleshores els plans estallen 2 a 2.


3. Si $a=1$:

    $$ A=\left(
    \begin{array}{ccc}
     1 & 1 & 1\\
     2 & 1 & 0\\
     1 & 1 & 1
    \end{array}
    \right)
    \qquad
    \left(
    \begin{array}{ccc|c}
    1 & 1 & 1 & 1\\
    2 & 1 & 0 & 1\\
    1 & 1 & 1 & 1
    \end{array}
    \right)
    $$

    Aquí, Rang $A=$ Rang $MA=2$, per tant el sistema és compatible indeterminat i els 3 plans es tallen en una recta. De fet, ja veiem que el primer i el tercer pla són coincidents.

####Angle entre dos plans

L'angle $\alpha$ entre dos plans ve donat per l'angle entre els seus vectors normals (que és el mateix que l'angle entre dos dels seus vectors directors).

Si considerem dos plans d'equacions: $\pi_1 \equiv A_1x+B_1y+C_1z+D_1=0$ i $\pi_2 \equiv A_2x+B_2y+C_2z+D_2=0$ amb vectors normals $\overrightarrow{ n_1 }=(A_1,B_1,C_1)$ i $\overrightarrow{ n_2 }=(A_2,B_2,C_2)$ tenim que:


$$\cos(\alpha)=\frac{ |\overrightarrow{ n_1 }\cdot \overrightarrow{ n_2 }| }{ |\overrightarrow{ n_1 }|\cdot |\overrightarrow{ n_2 }|}=\frac{ |A_1 A_2+B_1 B_2+ C_1 C_2+ D_1 D_2| }{ \sqrt{ A_1^2+B_1^2+C_1^2 }\cdot \sqrt{ A_2^2+B_2^2+C_2^2 }}$$

###Feix de plans d'aresta r

Donats dos plans d'equacions $\pi_1 \equiv A_1x+B_1y+C_1z+D_1=0$ i $\pi_2 \equiv A_2x+B_2y+C_2z+D_2=0$, el sistema format per les dues equacions representarà l'equació d'una recta si aquests dos plans no són paral.lels. Dit d'una altra manera, el sistema que formen haurà de ser __compatible determinat__ amb 1 paràmetre.

El feix de plans d'aresta $r$ ve determinat per tots aquells plans que es tallen en una mateixa línia de punts determinada per la recta. Per tant, la seva equació serà necessàriament __combinació lineal__ de les equacions dels dos plans inicials:


$$\alpha (A_1x+B_1y+C_1z+D_1)+ \beta (A_2x+B_2y+C_2z+D_2)=0 \forall \alpha, \beta \in \mathbb{ R }$$

En el cas que $\beta \ne 0$, podem dividir l'expressió anterior per $\beta$ i obtenim:

$$\frac{ \alpha }{ \beta } (A_1x+B_1y+C_1z+D_1)+ A_2x+B_2y+C_2z+D_2=0$$

I si fem un canvi de nom, $\lambda \equiv \frac{ \alpha }{ \beta }$:

$$\lambda (A_1x+B_1y+C_1z+D_1)+ A_2x+B_2y+C_2z+D_2=0$$

és l'equació del feix de plans d'aresta $r$.

En el cas que $\beta$ fos zero, només hi hauria un pla en el feix, i aquest seria lògicament $\pi_1$.

__Exemple 11__

Troba l'equació del pla que conté la recta:

$$r: \begin{cases} 3x+z&=0 \\ 2x+y&=-1  \end{cases}$$

i que passa pel punt $P(1,0,0)$.


L'equació de la recta $r$ està formada per les equacions de dos plans. Primer de tot ens caldrà comprovar si el punt $P$ que ens donen forma part d'algun dels dos plans substituïnt les seves coordenades en l'equació de cadascun dels plans (i en aquest cas ja hauríem acabat). Veiem que no compleix cap de les equacions, per tant, ens caldrà escriure el feix de plans d'aresta $r$ i trobar la combinació lineal que passa pel punt $P$. El feix de plans ve donat per l'expressió:

$$\lambda (3x+z)+ 2x+y+1=0$$

Si substituïm les coordenades del punt $P$ en l'expressió anterior obtenim:

$$\lambda (3\cdot 1+0)+2\cdot 1+1=0\rightarrow \lambda= -1$$

Per tant, el pla que ens demanen és:

$$x-y+z-1=0$$
