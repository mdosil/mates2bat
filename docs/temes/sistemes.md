#Tema 6: Sistemes d'equacions

##Sistemes d'equacions lineals

Expressem un sistema lineal de $m$ equacions i $n$ incògnites com:



$$
\begin{cases} a_{11} x_1 + a_{12} x_2 + ... + a_{1n} x_n = b_1 \\ a_{21} x_1 + a_{22} x_2 + ... + a_{2n} x_n = b_2 \\ ... \\ a_{m1} x_1 + a_{m2} x_2 + ... + a_{mn} x_n = b_m \end{cases}
$$


Donat aquest sistema, definim la seva matriu associada, $A$, a la matriu que conté els coeficients de les incògnites, i la seva matriu ampliada, $MA$, a la matriu que conté els coeficients de les incògnites més els termes independents:


$$
A=\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n}\\
a_{21} & a_{22} & a_{23} &...& a_{2n}\\
a_{31} & a_{32} & a_{33} &...& a_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
a_{m1} & a_{m2} & a_{m3} &...& a_{mn}\\
\end{pmatrix}
\quad
MA=\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n} & b_1\\
a_{21} & a_{22} & a_{23} &...& a_{2n} & b_2\\
a_{31} & a_{32} & a_{33} &...& a_{3n} & b_3\\
. & . & . &.& . &.\\
. & . & . &.& .& .\\
. & . & . &.& .& .\\
a_{m1} & a_{m2} & a_{m3} &...& a_{mn} & b_m\\
\end{pmatrix}
$$

###Solució d'un sistema d'equacions lineal. Classificació segons el nombre de solucions

Trobar solució per un sistema significa trobar els valors de les incògnites $x_{1}, x_{2},..., x_{n}$ que fan certes totes i cadascuna de les igualtats. Això no sempre és possible, és per això que es classifiquen el sistemes segons:

* __Sistemes compatibles__. Són aquells que tenen solució. Podem trobar també dos casos:
    * __Sistemes compatibles determinats__. Tenen una __única solució__ (això és, un únic conjunt de valors $x_{1}, x_{2},..., x_{n}$ que satisfà totes les igualtats).
    * __Sistemes compatibles indeterminats__. Tenen __infinites solucions__.

* __Sistemes incompatibles__. No tenen solució.

Pel que fa a les solucions, diem que dos sistemes són __equivalents__ si tenen la mateixa solució.



##Teorema de Rouché-Frobënius

L'enunciat del teorema ens diu el següent:

> Un sistema només és __compatible__ si rang$M$=rang$MA$.

>Si rang$M$=rang$MA$=$r=n$, on $n$ és el nombre d'incògnites, el sistema és __compatible determinat__

>Si rang$M$=rang$MA$=$r<n$, el sistema és __compatible indeterminat__ amb $n-r$ graus de llibertat.


##Notació matricial d'un sistema

Podem expressar el sistema anterior com un producte de dues matrius:

$$AX=B$$

on $A$ és la matriu de coeficients del sistema, $X$ és el vector columna amb les incògnites i $B$ és el vector columna amb els termes independents:

$$
A=\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n}\\
a_{21} & a_{22} & a_{23} &...& a_{2n}\\
a_{31} & a_{32} & a_{33} &...& a_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
a_{m1} & a_{m2} & a_{m3} &...& a_{mn}\\
\end{pmatrix}
\quad
X=\begin{pmatrix}
x_{1}\\
x_{2}\\
x_{3}\\
. \\
. \\
. \\
x_{n}\\
\end{pmatrix}
\quad
B=\begin{pmatrix}
b_{1}\\
b_{2}\\
b_{3}\\
. \\
. \\
. \\
b_{n}\\
\end{pmatrix}
$$

Per tant:

$$
A\cdot X=B \rightarrow
\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n}\\
a_{21} & a_{22} & a_{23} &...& a_{2n}\\
a_{31} & a_{32} & a_{33} &...& a_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
a_{m1} & a_{m2} & a_{m3} &...& a_{mn}\\
\end{pmatrix}
\cdot
\begin{pmatrix}
x_{1}\\
x_{2}\\
x_{3}\\
. \\
. \\
. \\
x_{n}\\
\end{pmatrix}
=
\begin{pmatrix}
b_{1}\\
b_{2}\\
b_{3}\\
. \\
. \\
. \\
b_{n}\\
\end{pmatrix}
$$

##Mètodes de resolució de sistemes lineals

###Mètode de la inversa

Tornant a l'expressió d'un sistema com una equació matricial, aquesta la podem transformar de la manera següent:

\begin{aligned}
A\cdot X &= B \\
A^{-1}\cdot A \cdot X &= A^{-1}\cdot B\\
\mathbb{1}X &= A^{-1}\cdot B\\
X &= A^{-1}\cdot B\\
\end{aligned}

Per tant, per trobar la solució d'un sistema només ens cal buscar la matriu inversa i multiplicar-la pel vector columna de termes independents. Aquest mètode només és útil per aquelles matrius $A$ tals que $|A|\ne 0$. Això implica que el rang de la matriu i la matriu ampliada coincideixen i és igual al nombre d'incògnites. Per tant, és un sistema compatible determinat.

__Exemple 1__

Troba la solució del sistema lineal següent:

$$
\begin{cases} 2x+y-z=3 \\ x-y+z=1 \\ 3x+y=4 \end{cases}
$$

Primer de tot expressarem la matriu i matriu ampliada del sistema:

$$
A=\begin{pmatrix}
2 & 1 & -1\\
1 & -1 & 1\\
3 & 1 & 0
\end{pmatrix}
\quad
MA=\begin{pmatrix}
2 & 1 & -1 & 3\\
1 & -1 & 1 & 1\\
3 & 1 & 0 & 4
\end{pmatrix}
$$

Ens cal ara estudiar el rang de la matriu $A$ i la matriu $MA$ per veure si el sistema té solució o no. Com que ja tenim un element diferent de zero, el rang de la matriu $A$ com a mínim és 1. Anem a buscar un menor d'ordre dos no nul:

$$
\begin{vmatrix}
2 & 1\\
1 & -1
\end{vmatrix}
=-3 \ne 0
$$

El rang per tant, com a mínim és 2. Anem a calcular el determinant de la matriu:

$$
A=\begin{vmatrix}
2 & 1 & -1\\
1 & -1 & 1\\
3 & 1 & 0
\end{vmatrix}
=-3\ne 0
$$

Veiem que rang$A=3$ i necessàriament serà igual al rang de la matriu ampliada (perquè conté el menor de la matriu $A$ a dins). Per tant, aquest sistema és compatible determinat. Anem ara a trobar la solució. En forma matricial:


$$
\begin{pmatrix}
2 & 1 & -1\\
1 & -1 & 1\\
3 & 1 & 0
\end{pmatrix}
\cdot
\begin{pmatrix}
x \\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
3\\
1\\
4
\end{pmatrix}
$$

Per trobar la solució cal que fem: $X=A^{-1}\cdot B$. Anem a buscar primer la inversa de la matriu, $A^{-1}=\frac{ 1 }{ |A| } Adj(A)^{T}$:

$$
Adj(A)=\begin{pmatrix}
-1 & 3 & 4\\
-1 & 3 & 1\\
2 & -3 & -3
\end{pmatrix}
\Rightarrow
Adj(A)^{T}=\begin{pmatrix}
-1 & -1 & 2\\
3 & 3 & -3\\
4 & 1 & -3
\end{pmatrix}
\Rightarrow
A^{-1}=\frac{ -1 }{ 3 }\begin{pmatrix}
-1 & -1 & 2\\
3 & 3 & -3\\
4 & 1 & -3
\end{pmatrix}
$$

Per tant:

$$
X=
\frac{ -1 }{ 3 }\begin{pmatrix}
-1 & -1 & 2\\
3 & 3 & -3\\
4 & 1 & -3
\end{pmatrix}
\cdot
\begin{pmatrix}
3\\
1\\
4
\end{pmatrix}
=
\begin{pmatrix}
-4/3\\
0\\
-1/3
\end{pmatrix}
$$

La solució d'aquest sistema és:

$$x=\frac{ -4 }{ 3 }\qquad y=0 \qquad z=\frac{ -1 }{ 3 }$$


###Mètode de Gauss

El mètode de Gauss es basa en la [triangulació de matrius](http://mdosil.cat/mates2batcientific/temes/matrius/#triangulacio-de-matrius) que havíem vist en el tema anterior. Farem el següent:

1. Escriurem la matriu $A$ de coeficients (cal vigilar que les incògnites estiguin aliniades de tal manera que la mateixa columna d'una matriu correspongui a una mateixa incògnita) i la matriu ampliada del sistema afegint la columna de termes independents, $MA$.
2. Amb la matriu ampliada, intentarem aconseguir que l'element $a_{11}$, el coeficient de la primera equació i la primera incògnita, sigui $1$. Si no ho és, intentarem aconseguir-ho amb operacions fila.
3. Primer de tot, mitjançant operacions fila, aconseguirem que els elements sota $a_{11}$ siguin zero.
4. Un cop aconseguit això, farem el mateix a la segona columna per obtenir els elements $a_{12}$ i $a_{22}$ diferents de zero i la resta de la columna zero.
5. Continuarem el procediment fins aconseguir una matriu triangular (tot i que treballem amb la matriu ampliada).
6. Expressarem la matriu altra vegada en forma d'equació lineal i trobarem les incògnites successives substituïnt de baix a dalt, tal i com veurem amb l'exemple següent.

__Exemple 2__

Resol el sistema de l'exemple 1 pel mètode de Gauss.

Ja hem vist que és un sistema compatible determinat. Anem a triangular doncs la matriu:


$$ \left(
\begin{array}{ccc|c}
  2 & 1 & -1 & 3\\
  1 & -1 & 1 & 1\\
  3 & 1 & 0 & 4
\end{array}
\right)
$$

Intercanviem les files 1 i 2:

$$ \left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  2 & 1 & -1 & 3\\
  3 & 1 & 0 & 4
\end{array}
\right)
$$

A la fila 2 li restem dues vegades la fila 1 i a la fila 3 li restem 3 vegades la fila 1:

$$ \left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  0 & 3 & -3 & 1\\
  0 & 4 & -3 & 1
\end{array}
\right)
$$

Finalment, a la fila 3 li restem $\frac{ 4 }{ 3 }$ la fila 2:

$$ \left(
\begin{array}{ccc|c}
  1 & -1 & 1 & 1\\
  0 & 3 & -3 & 1\\
  0 & 0 & 1 & -\frac{ 1 }{ 3 }
\end{array}
\right)
$$

Tornem a escriure l'equació:

$$
\begin{cases} x-y+z= 1 \\ 3y-3z = 1 \\ z= -\frac{ 1 }{ 3 } \end{cases}
$$

Ja hem trobat la última incògnita. Ara farem una substitució retroactiva: substituïnt $z$ a la segona equació obtindrem $y$. I finalment ens quedarà substituir $z$ i $y$ a la primera equació per obtenir $x$. Amb això tenim que:

$$x=\frac{ -4 }{ 3 }\qquad y=0 \qquad z=\frac{ -1 }{ 3 }$$

Aquest sistema era de fàcil solució perquè era compatible determinat. Si després de resoldre ens trobem amb una fila de zeros, voldrà dir que una equació és combinació lineal de les altres dues, per tant, hi ha més incògnites que equacions i el sistema seria compatible indeterminat. Per acabar, si arribem a una igualtat del tipus $0=b$, tindríem que el sistema és incompatible.

###Mètode de Cramer

Un sistema quadrat $nxn$ direm que és de Cramer si el determinant de la matriu de coeficients és diferent de zero: $|A|\ne 0$ (i per tant el sistema és compatible determinat).

Per simplicitat, anem a explicar-ho per un sistema 3x3 de 3 equacions i 3 incògnites. Sigui $\Delta_{x}$ el determinant que s'aconsegueix substituïnt al determinant de la matriu de coeficients la primera columna per la de termes independents. El mateix per $\Delta_{y}$ (determinant que s'aconsegueix substituïnt al determinant de la matriu de coeficients la segona coluimna per la de termes independents) i $\Delta_{z}$. La solució del sistema d'equacions ve donada per les expressions:

$$
x=\frac{ \Delta_{x} }{ |A| }\qquad y=\frac{ \Delta_{y} }{ |A| }\qquad z=\frac{ \Delta_{z} }{ |A| }
$$

__Exemple 3__

Resol el sistema de l'exemple 1 pel mètode de Cramer.

De l'exemple 1 teníem:

$$|A|=-3\ne 0$$

Anem a trobar el resultat de les incògnites:

$$
x=\frac{ \begin{vmatrix}
3 & 1 & -1\\
1 & -1 & 1\\
4 & 1 & 0
\end{vmatrix} }{ |A| }
=-\frac{ 4 }{ 3 }
\qquad
y=\frac{ \begin{vmatrix}
2 & 3 & -1\\
1 & 1 & 1\\
3 & 4 & 0
\end{vmatrix} }{ |A| }
=0
\qquad
z=\frac{ \begin{vmatrix}
2 & 1 & 3\\
1 & -1 & 1\\
3 & 1 & 4
\end{vmatrix} }{ |A| }
=-\frac{ 1 }{ 3 }
$$


##Mètode de resolució general de sistemes

Anem a donar aquí un mètode per a resoldre sistemes i al final en farem un exemple.

1. Aplicarem el teorema de Rouché Frobënius per mirar el tipus de solucions que té el sistema.
2. Si el sistema és incompatible (Rang $A\ne$ Rang $MA$) ja hem acabat.
3. Si el sistema és compatible determinat (Rang $A=$ Rang $MA=$ nombre d'incògnites) utilitzarem qualsevol dels 3 mètodes, tot i que el mètode de Cramer sovint és el més ràpid.
4. Si el sistema és compatible indeterminat (Rang $A=$ Rang $MA <$ nombre d'incògnites) sortirà una solució amb paràmetres. En aquest cas el mètode més pràctic és el de Gauss tot i que també es podria arribar a resoldre per Cramer (el mètode de la inversa no perquè el determinant de la matriu és zero).

En l'exemple 1, vèiem un sistema compatible determinat. Anem a veure ara un parell d'exemples pels altres 2 tipus de sistemes.

__Exemple 4 : sistema incompatible__

Resol el sistema següent:

$$
\begin{cases} 2x+3y+z=4 \\ x-2y+z=-2 \\ 8x+5y+5z=1 \end{cases}
$$

Anem a construir la matriu $A$ i la matriu ampliada, $MA$. A partir d'aquí, estudiarem els seus rangs.

$$
A=\begin{pmatrix}
2 & 3 & 1\\
1 & -2 & 1\\
8 & 5 & 5
\end{pmatrix}
\qquad
MA=\begin{pmatrix}
2 & 3 & 1 & 4\\
1 & -2 & 1 & -2\\
8 & 5 & 5 & 1
\end{pmatrix}
$$

El rang de la matriu $A$ com a mínim és 1 perquè té un element diferent de zero. Orlem l'element $a_{11}$ i mirem si té algun menor d'ordre 2 diferent de zero:

$$
\begin{vmatrix}
2 & 3\\
1 & -2
\end{vmatrix}
=-7
$$
Per tant, el rang de $A$ com a mínim és 2. Anem a calcular el menor d'ordre 3:

$$
\begin{vmatrix}
2 & 3 & 1\\
1 & -2 & 1\\
8 & 5 & 5
\end{vmatrix}
=0
$$

La matriu $A$ té rang 2. Anem a orlar el menor d'ordre 2 amb la columna de termes independents per veure quin rang té la matriu ampliada:

$$
\begin{vmatrix}
2 & 3 & 4\\
1 & -2 & -2\\
8 & 5 & 1
\end{vmatrix}
=15
$$

Veiem que el rang de la matriu ampliada és 3. Com que els 2 rangs no són iguals, tenim un __sistema incompatible__.

A la pràctica, si l'haguéssim intentat resoldre per Gauss sense mirar els rangs, després de triangular ens hagués quedat alguna igualtat del tipus $0=k$ on $k$ és un nombre diferent de zero. Com que aquesta igualtat mai pot ser certa, el sistema és incompatible.

__Exemple 5: sistema compatible indeterminat__

Resol el sistema següent:

$$
\begin{cases} x+2y+z=1 \\ 2x-y-4z=0 \\ 3x+y-3z=1 \end{cases}
$$

Anem a construir la matriu $A$ i la matriu ampliada, $MA$. A partir d'aquí, estudiarem els seus rangs.

$$
A=\begin{pmatrix}
1 & 2 & 1\\
2 & -1 & -4\\
3 & 1 & -3
\end{pmatrix}
\qquad
MA=\begin{pmatrix}
1 & 2 & 1 & 1\\
2 & -1 & -4 & 0\\
3 & 1 & -3 & 1
\end{pmatrix}
$$

El rang de la matriu $A$ com a mínim és 1 perquè té un element diferent de zero. Orlem l'element $a_{11}$ i mirem si té algun menor d'ordre 2 diferent de zero:


$$
\begin{vmatrix}
1 & 2\\
2 & -1
\end{vmatrix}
=-5
$$
Per tant, el rang de $A$ com a mínim és 2. Anem a calcular el menor d'ordre 3:

$$
\begin{vmatrix}
1 & 2 & 1\\
2 & -1 & -4\\
3 & 1 & -3
\end{vmatrix}
=0
$$

La matriu $A$ té rang 2. Anem a orlar el menor d'ordre 2 amb la columna de termes independents per veure quin rang té la matriu ampliada:

$$
\begin{vmatrix}
1 & 2 & 1\\
2 & -1 & 0\\
3 & 1 & 1
\end{vmatrix}
=0
$$

Veiem que el rang de la matriu ampliada també és 2. Els dos rangs són iguals però són més petits que el nombre d'incògnites, que és 3. Per tant és un sistema compatible indeterminat amb un paràmetre. Anem a resoldre el sistema pel mètode de Gauss i expressarem les solucions possibles en funció d'aquest paràmetre.

$$ \left(
\begin{array}{ccc|c}
  1 & 2 & 1 & 1\\
  2 & -1 & -4 & 0\\
  3 & 1 & -3 & 1
\end{array}
\right)
$$

A la fila 2 li restem dues vegades la fila 1 i a la fila 3 li restem 3 vegades la fila 1:

$$ \left(
\begin{array}{ccc|c}
  1 & 2 & 1 & 1\\
  0 & -5 & -6 & -2\\
  0 & -5 & -6 & -2
\end{array}
\right)
$$

I ara a la fila 3 li restem la fila 2:

$$ \left(
\begin{array}{ccc|c}
  1 & 2 & 1 & 1\\
  0 & -5 & -6 & -2\\
  0 & 0 & 0 & 0
\end{array}
\right)
$$

Veiem que obtenim una fila de zeros. Això sempre passa quan el sistema és compatible indeterminat. Aquest sistema ens queda:

$$
\begin{cases} x+2y+z=1 \\ -5y-6z=-2 \end{cases}
$$

Com que el rang és 2 i tenim 3 incògnites, això voldrà dir que hi ha un paràmetre (nombre real). El que es fa és assignar aquest paràmetre a una de les variables i expressar les altres en funció d'aquest valor. En el nostre cas, farem:

$$
z=\lambda \qquad y=\frac{ 2-6\lambda }{ 5 } \qquad x=\frac{ 1-7\lambda }{ 5 }
$$

##Sistemes homogenis

Els sistemes homogenis són aquells els quals els termes independents són sempre zero. Així doncs, la matriu ampliada serà igual a la matriu més una columna de zeros. Això vol dir que el rang de la matriu i la matriu ampliada són iguals i per tant, els sistemes homogenis, sempre són compatibles.

D'altra banda, aquests sistemes sempre tenen la solució on totes les incògnites són 0 (solució trivial). Ens caldrà només estudiar el rang de la matriu, si aquest és igual al nombre d'incògnites, el sistema és compatible determinat i la solució no és altra que la solució trivial. Si el rang de la matriu és menor al nombre d'incògnites, el sistema serà compatible indeterminat i llavors caldrà expressar les solucions en funció de paràmetres.

__Exemple 6__

Resol el sistema següent:

$$
\begin{cases} x-y+z=0 \\ 2x+y-z=0 \\ y+z=0 \end{cases}
$$

Anem a estudiar el rang de la matriu de coeficients $A$:

$$
\begin{vmatrix}
1 & -1\\
2 & 1
\end{vmatrix}
=4
$$

El rang com a mínim és 2. Anem a calcular el menor d'ordre 3:

$$
\begin{vmatrix}
1 & -1 & 1\\
2 & 1 & -1\\
0 & 1 & 1
\end{vmatrix}
=6
$$

Per tant, el rang de la matriu i de la matriu ampliada és 3, el sistema és compatible determinat. La seva solució és la solució trivial:

$$
x=0 \qquad y=0 \qquad z=0
$$


##Discussió de sistemes segons el valor d'un paràmetre

Anem a il.lustrar aquest punt amb un exemple extret de les [PAU juny 2014.](http://universitats.gencat.cat/web/.content/01_acces_i_admissio/pau/documents/examens_2014/pau_mate14jl.pdf)

Considera el sistema següent:

$$
\begin{cases} (k-1)y+(k^2-1)z=0 \\ (4k+1)x-y-7z=1 \\ x+y+z=0 \end{cases}
$$

on $k \in \mathbb{R}$

1. Discutiu el sistema d'equacions lineals en funció dels valors de $k$.
2. Resoleu el sistema per $k=1$

Escrivim la matriu $A$ i la matriu ampliada, $MA$. Anem a estudiar el rang d'ambdues i aplicarem el teorema de Rouché Frobënius per a saber de quin tipus és segons les seves solucions.

$$
A=\begin{pmatrix}
0 & k-1 & k^2-1\\
4k+1 & -1 & -7\\
1 & 1 & 1
\end{pmatrix}
\qquad
MA=\begin{pmatrix}
0 & k-1 & k^2-1 & 0\\
4k+1 & -1 & -7 & 1\\
1 & 1 & 1 & 0
\end{pmatrix}
$$

El rang de la matriu $A$ com a mínim és 1. Veiem ara si té algun menor d'ordre 2 diferent de zero:

$$
\begin{vmatrix}
-1 & -7\\
1 & 1
\end{vmatrix}
=5
$$

El rang com a mínim és 2. Anem a calcular el menor d'ordre 3. Ho fem desenvolupant per la 1a fila:

$$
\begin{vmatrix}
0 & k-1 & k^2-1\\
4k+1 & -1 & -7\\
1 & 1 & 1
\end{vmatrix}
=-(k-1)
\begin{vmatrix}
4k+1 & -7 \\
1 & 1
\end{vmatrix}
+(k^2-1)
\begin{vmatrix}
4k+1 & -1 \\
1 & 1
\end{vmatrix}
=(1-k)(4k+1+7)+(k^2-1)(4k+1+1)=...=(k-1)(4k^2+2k-6)
$$

En aquest punt hem de distinguir entre 2 casos. Hi ha el cas en que el determinant de la matriu és zero (i això voldrà dir que el rang de la matriu $A$ és 2) i el cas que aquest determinant és diferent de zero:

Si $|A|=0$ tenim que:

$$(k-1)(4k^2+2k-6)=0 \rightarrow k=1 \qquad k=-\frac{ 3 }{ 2 } $$

Anem a desglossar els 3 casos:

* $k=1$:
    Caldrà estudiar el rang de la matriu ampliada. Fem $k=1$ i orlem el menor d'ordre 2 amb la columna de termes independents:

    $$
    \begin{vmatrix}
    0 & 0 & 0\\
    -1 & -7 & 1\\
    1 & 1 & 0
    \end{vmatrix}
    =0
    $$

    En aquest cas, el rang de la matriu ampliada també és 2. Per tant:

    __Rang $A=$ Rang $MA=2 \rightarrow$ Sistema Compatible Indeterminat__

* $k=-\frac{3}{2}$:

    Anem a veure el rang de la matriu ampliada. Fem $k=-\frac{ 3 }{ 2 }$ i orlem el menor d'ordre 2 amb la columna de termes independents:

    $$
    \begin{vmatrix}
    -\frac{ 5 }{ 2 }  & \frac{ 5 }{ 4 } & 0\\
    -1 & -7 & 1\\
    1 & 1 & 0
    \end{vmatrix}
    =\frac{ 15 }{ 4 } \ne 0
    $$

    En aquest cas, el rang de la matriu ampliada és 3. Per tant:

    __Rang $A\ne$ Rang $MA \rightarrow$ Sistema Incompatible__

* $k \ne 1$ o $k\ne -\frac{ 3 }{ 2 }$:

    __Rang $A=$ Rang $MA=3\rightarrow$ Sistema Compatible Determinat__

Anem a resoldre el sistema per $k=1$. Ho farem pel mètode de Gauss:

$$ \left(
\begin{array}{ccc|c}
  0 & 0 & 0 & 0\\
  5 & -1 & -7 & 1\\
  1 & 1 & 1 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & 1 & 1 & 0\\
  5 & -1 & -7 & 1\\
  0 & 0 & 0 & 0
\end{array}
\right)
=
\left(
\begin{array}{ccc|c}
  1 & 1 & 1 & 0\\
  0 & -6 & -12 & 1\\
  0 & 0 & 0 & 0
\end{array}
\right)
$$

Això dóna lloc al sistema:


$$
\begin{cases} x+y+z=0 \\ -6y-12z=1 \end{cases}
$$

El sistema és compatible indeterminat amb un paràmetre. Si agafem $z=\lambda$ tenim la solució:

$$
z=\lambda \qquad y=\frac{ -12\lambda-1 }{ 6 } \qquad x=\frac{ 6\lambda+1 }{ 6 }
$$
