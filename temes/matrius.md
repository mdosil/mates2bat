#Tema 5: Matrius i determinants

##Definició: matrius i tipus de matrius

S'anomena matriu de dimensió $m x n$ a qualsevol taula de nombres que consti de $m$ files i $n$ columnes.

L'expressió $m x n$ s'anomena dimensió o ordre de la matriu.

Anem a veure alguns exemples:

<!---
$$
\begin{matrix}
a & b \\
c & d
\end{matrix}
\quad
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\quad
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\quad
\begin{vmatrix}
a & b \\
c & d
\end{vmatrix}
\quad
\begin{Vmatrix}
a & b \\
c & d
\end{Vmatrix}
$$

--->

$$A_{3x2}=\begin{pmatrix}
1 & 0 \\
0 & -1\\
5 & 7
\end{pmatrix}
\quad
B_{2x3}=\begin{pmatrix}
1 & 0 & 5\\
0 & -1 & 7
\end{pmatrix}
\quad
C_{3x3}=\begin{pmatrix}
1 & 0 & 5\\
0 & -1 & 7 \\
4 & 3 & 8\\
\end{pmatrix}
$$

En general, per parlar de matrius $mxn$ utilitzarem la notació:

$$
A=(a_{ij})=\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n}\\
a_{21} & a_{22} & a_{23} &...& a_{2n}\\
a_{31} & a_{32} & a_{33} &...& a_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
a_{n1} & a_{n2} & a_{n3} &...& a_{nn}\\
\end{pmatrix}
\quad
\begin{matrix}
i=1,2,...,m \\
j=1,2,...,n
\end{matrix}
$$

L'índex $i$ normalment s'utilitza per les files i l'índex $j$ per les columnes.

###Tipus de matrius

1. __Matriu quadrada__

    Diem que una matriu és quadrada quan té el mateix nombre de files que de columnes ($nxn$):

    $$A=\begin{pmatrix}
    2 & 3 \\
   -1 & 5
   \end{pmatrix}$$

    és una matriu d'ordre $2$ i

    $$B=\begin{pmatrix}
    0 & 3 & 5\\
    2 & 5 & 8 \\
    4 & -3 & 0
    \end{pmatrix}$$

    és una matriu d'ordre $3$.

    La diagonal de les matrius quadrades s'anomena __diagonal principal__.


2. __Vector fila__


    És una matriu que només té una fila:


    $$u_{1x5}=\begin{pmatrix}
    0 & 5 & 3 & 2 & 8
    \end{pmatrix}$$


3. __Vector columna__

    És una matriu que només té una columna:



    $$v_{5x1}=\begin{pmatrix}
    2 \\
    -1 \\
    3 \\
    8\\
    4
    \end{pmatrix}$$


4. __Matriu nul.la__

    És una matriu on tots els seus elements són $0$:

    $$A_{3x2}=\begin{pmatrix}
    0 & 0 \\
    0 & 0\\
    0 & 0
    \end{pmatrix}
    \quad
    B_{2x3}=\begin{pmatrix}
    0 & 0 & 0\\
    0 & 0 & 0
    \end{pmatrix}$$

5. __Matriu diagonal__

    És una matriu quadrada que només té elements no nuls a la diagonal:


    $$\begin{pmatrix}
    1 & 0 & 0 \\
    0 & 2 & 0\\
    0 & 0 & -1
    \end{pmatrix}
    \quad
    \begin{pmatrix}
    2 & 0\\
    0 & 1
    \end{pmatrix}$$

6. __Matriu unitat__

    És una matriu diagonal on tots els elements de la diagonal principal són $1$:

    $$\mathbb{1}_{3x3}=\begin{pmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0\\
    0 & 0 & 1
    \end{pmatrix}
    \quad
    \mathbb{1}_{4x4}=\begin{pmatrix}
    1 & 0 & 0 & 0\\
    0 & 1 & 0 & 0\\
    0 & 0 & 1 & 0 \\
    0 & 0 & 0 & 1
    \end{pmatrix}$$

7. __Matriu triangular__

    Matriu quadrada on tots els elements situats per sobre o per sota la diagonal principal valen $0$:

    $$\begin{pmatrix}
    8 & 0 & 0 \\
    -5 & 4 & 0\\
    3 & -10 & 1
    \end{pmatrix}
    \quad
    \begin{pmatrix}
    15 & 23 & -2 & 8\\
    0 & 2 & 3 & 25\\
    0 & 0 & 1 & 13 \\
    0 & 0 & 0 & -5
    \end{pmatrix}$$

8. __Matriu transposta d'una matriu $A$__

    Donada una matriu $A$, de dimensió $mxn$, la seva transposta és aquella matriu $A^T$ (transposta d'$A$), de dimensió $nxm$ obtinguda al canviar files per columnes:

    $$A=\begin{pmatrix}
    2 & 5 & 0 \\
    -1 & 3 & 7
    \end{pmatrix}
    \quad
    A^T=\begin{pmatrix}
    2 & -1\\
    5 & 3\\
    0 & 7\\
    \end{pmatrix}$$

9. __Matriu oposada d'una matriu $A$__

    Donada una matriu $A$, de dimensió $mxn$, la seva oposada és aquella matriu $-A$, que s'obté canviant de signe tots els elements de $A$:

    $$A=\begin{pmatrix}
    2 & 5 & 0 \\
    -1 & 3 & 7
    \end{pmatrix}
    \quad
    -A=\begin{pmatrix}
    -2 & -5 & 0\\
    -1 & -3 & -7
    \end{pmatrix}$$

10. __Matriu simètrica__

    Donada una matriu quadrada $A$, de dimensió $nxn$, direm que és simètrica si els seus elements verifiquen $a_{ij}=a{ji} \forall i,j$:

    $$A=\begin{pmatrix}
    1 & 3 & 5 \\
    3 & 4 & 2\\
    5 & 2 & 0
    \end{pmatrix}
    $$

    Una matriu $A$ és simètrica si $A^T=A$.

11. __Matriu antisimètrica__

    Donada una matriu quadrada $A$ de dimensió $nxn$, direm que és antisimètrica si els seus elements verifiquen $a_{ij}=-a{ji} \forall i,j$:

    $$A=\begin{pmatrix}
    0 & -3 & 5 \\
    3 & 0 & -2\\
    -5 & 2 & 0
    \end{pmatrix}
    $$

    Una matriu $A$ és antisimètrica si $A^T=-A$. Per tant, totes les matrius antisimètriques tenen zeros a la seva diagonal.

##Operacions amb matrius

###Suma de matrius d'igual dimensió

Per sumar dues matrius cal que tinguin la mateixa dimensió. Llavors sumarem terme a terme:


$$
\begin{matrix}
 (a_{ij})& +(b_{ij}) & =(a_{ij}+b_{ij})\\
mxn & mxn & mxn
\end{matrix}$$

Per restar dues matrius, l'únic que hem de fer és sumar a la primera l'oposada de la segona matriu.

__Exemple 1__

$$\begin{pmatrix}
1 & 0 \\
-2 & 1\\
3 & 1
\end{pmatrix}
+
\begin{pmatrix}
0 & 7 \\
1 & 2\\
0 & -1
\end{pmatrix}
=
\begin{pmatrix}
1 & 7 \\
-1 & 3\\
3 & 0
\end{pmatrix}
$$

####Propietats de la suma de matrius

1. Associativa

    $$(A+B)+C=A+(B+C)$$

2. Commutativa

    $$A+B=B+A$$

3. Element neutre

    És la matriu nul.la perquè sumada a qualsevol matriu la deixa invariant.

4. Element oposat

    L'element oposat a una matriu $A$ és la matriu $-A$ perquè sumades donen l'element neutre.

###Producte d'una matriu per un nombre

Per multiplicar una matriu per un nombre real, multiplicarem cada element de la matriu per aquest nombre:

$$
\begin{matrix}
 \alpha \cdot (a_{ij})& =(\alpha \cdot a_{ij})\\
mxn & mxn
\end{matrix}$$

###Producte de matrius

####Producte d'un vector fila per un vector columna

El producte d'un vector fila per un vector columna es coneix com a __producte escalar__ i dóna lloc sempre a un nombre real. Per a fer-ho, el nombre de columnes del vector fila ha de ser el mateix que el nombre de files del vector columna. En general, si hem de multipicar un vector fila per un vector columna qualsevol:

$$
\begin{pmatrix}
a_{11} & a_{12} &...&a_{1n}
\end{pmatrix}
\cdot
\begin{pmatrix}
b_{11}\\
b_{21}\\
.\\
.\\
.\\
b_{n1}
\end{pmatrix}
=a_{11}b_{11}+a_{12}b_{21}+...+a_{1n}b_{n1}=\sum_{k=1}^{n} a_{1k}b_{k1}
$$

__Exemple 2__

$$
\begin{pmatrix}
1 & 3 & 2
\end{pmatrix}
\cdot
\begin{pmatrix}
-1\\
0\\
2
\end{pmatrix}
=1\cdot (-1)+3\cdot 0+2 \cdot 2=-1+0+4=3
$$

####Producte de dues matrius quadrades del mateix ordre

El producte de matrius quadrades és molt senzill. S'agafen els elements de la primera fila i es multipliquen pels elements de la primera columna, tal i com hem fet a l'apartat anterior. El resultat d'aquesta operació es col.loca en l'element $a_{11}$ de la matriu producte. Seguidament, s'agafa altra vegada el vector de la primera fila i es multiplica escalarment per la segona columna. El resultat es col.loca en l'element $a_{12}$ de la matriu producte. I així successivament fins a fer tots els productes. Anem a veure'n un exemple.


__Exemple 3__

$$
\begin{pmatrix}
2 & 3 & 4\\
0 & 1 & -2 \\
1 & 2 & 1
\end{pmatrix}
\cdot
\begin{pmatrix}
-1 & 2 & 1\\
3 & 4 & -2\\
2 & 0 & 1
\end{pmatrix}
=
\begin{pmatrix}
15 & 16 & 0\\
-1 & 4 & -4\\
7 & 10 & -2
\end{pmatrix}
$$

####Producte general de Matrius

Per tal que el producte de dues matrius $A$ i $B$ estigui definitm necessitem que __el nombre de columnes de la matriu $A$ sigui igual al nombre de files de la matriu $B$__. D'altra banda, si el producte $A\cdot B$ està definit, el producte $B \cdot A$ no té perquè estar-ho.

__Exemple 4__

$$
\begin{pmatrix}
2 & 3 & -4\\
-1 & 4 & 6
\end{pmatrix}
\cdot
\begin{pmatrix}
5 & 1 & 1\\
4 & -2 & 0 \\
0 & 3 & 0
\end{pmatrix}
=
\begin{pmatrix}
22 & -16 & 2\\
11 & 9 & -1
\end{pmatrix}
$$

Fixeu-vos que en aquest cas el producte invers no està definit perquè la segona matriu té 3 columnes i la primera dies files i per tant no es podrien multiplicar. Si les matrius són quadrades del mateix ordre els productes sempre estan definits.

####Propietats del producte de matrius

1. Associativa

    $$(A\cdot B)\cdot C=A\cdot (B\cdot  C)$$

2. Commutativa

    No la verifica. En general:

    $$A\cdot B\ne B\cdot A$$

3. Element neutre

    És la matriu unitat: qualsevol matriu multiplicada per la matriu unitat és ella mateixa:

    $$A \cdot \mathbb{1}= \mathbb{1} \cdot A=A$$

    __Exemple 5__



    $$
    \begin{pmatrix}
    2 & 3 & 4\\
    0 & 1 & -2 \\
    1 & 2 & 1
    \end{pmatrix}
    \cdot
    \begin{pmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    0 & 0 & 1
    \end{pmatrix}
    =
    \begin{pmatrix}
    2 & 3 & 4\\
    0 & 1 & -2\\
    1 & 2 & 1
    \end{pmatrix}
    $$

4. Element invers

    Donada una matriu $A$, la seva matriu inversa és aquella matriu $A^{-1}$ tal que:

    $$A\cdot A^{-1}=\mathbb{1}$$

    No totes les matrius tenen inversa. El càlcul de la matriu inversa el deixem per a més endavant.

###Potència d'una matriu quadrada

En general, les potències d'una matriu quadrada es calculen segons:

\begin{align}
A^2&=A\cdot A\\
A^3&=A^2\cdot A=A\cdot A \cdot A\\
A^n&=A\cdot A \cdot A....\cdot A
\end{align}

##Determinants

###Determinants d'ordre 2

Donada una matriu quadrada $2x2$ podem definir el determinant d'aquesta matriu com l'operació:

$$
\begin{vmatrix}
a_{11} & a_{12}\\
a_{21} & a_{22}
\end{vmatrix}
=a_{11} \cdot a_{22} - a_{12} \cdot a_{21}
$$

El resultat d'un determinant sempre és un nombre real.

###Determinants d'ordre 3

També podem definir el determinant d'una matriu d'ordre 3:

$$
\begin{vmatrix}
a_{11} & a_{12} & a_{13}\\
a_{21} & a_{22} & a_{23}\\
a_{31} & a_{32} & a_{33}
\end{vmatrix}
=a_{11} \cdot a_{22} \cdot a_{33}+ a_{21} \cdot a_{32} \cdot a_{13} + a_{12} \cdot a_{23} \cdot a_{31}- a_{13} \cdot a_{22} \cdot a_{31} - a_{11} \cdot a_{23} \cdot a_{32} - a_{21} \cdot a_{12} \cdot a_{33}
$$

__Exemple 6__

Calcula els determinants següents:

$$
\begin{vmatrix}
2 & 3\\
4 & 5
\end{vmatrix}
=2 \cdot 5 -3 \cdot 4=-2
\quad
\begin{vmatrix}
2 & 3 & 5\\
4 & 5 & -1\\
3 & -2 & 1
\end{vmatrix}
=10-9-40-(75+12+4)=-130
$$


####Càlcul de determinants d'ordre tres desenvolupant per una fila o una columna

Podem transformar el càlcul de determinants d'ordre 3 de la manera següent:

\begin{align}
\begin{vmatrix}
a_{11} & a_{12} & a_{13}\\
a_{21} & a_{22} & a_{23}\\
a_{31} & a_{32} & a_{33}
\end{vmatrix}
&=a_{11} \cdot a_{22} \cdot a_{33}+ a_{21} \cdot a_{32} \cdot a_{13} + a_{12} \cdot a_{23} \cdot a_{31}- a_{13} \cdot a_{22} \cdot a_{31} - a_{11} \cdot a_{23} \cdot a_{32} - a_{21} \cdot a_{12} \cdot a_{33}\\
&=a_{11}(a_{22}a_{33}-a_{32}a_{23})-a_{12}(a_{21}a_{33}-a_{31}a_{23})+a_{13}(a_{21}a_{32}-a_{22}a_{31})\\
&=a_{11}
\begin{vmatrix}
a_{22} & a_{23}\\
a_{32} & a_{33}
\end{vmatrix}
- a_{12}
\begin{vmatrix}
a_{21} & a_{23}\\
a_{31} & a_{33}
\end{vmatrix}
+a_{13}
\begin{vmatrix}
a_{21} & a_{22}\\
a_{31} & a_{32}
\end{vmatrix}
\end{align}


__Exemple 7__


$$
\begin{vmatrix}
1 & 0 & 2\\
-3 & 1 & 0\\
1 & 0 & 1
\end{vmatrix}
=1\begin{vmatrix}
1 & 0\\
0 & 1
\end{vmatrix}
-0\begin{vmatrix}
-3 & 0\\
1 & 1
\end{vmatrix}
+2\begin{vmatrix}
-3 & 1\\
1 & 0
\end{vmatrix}
=-1
$$

##### Adjunt d'un element $a_{ij}$. Matriu adjunta

Intentarem d'expressar això d'una manera més formal. Definim $\alpha_{ij}$ com el __menor complementari__ d'un element $a_{ij}$ d'una matriu $A$ com aquell determinant d'ordre $2$ que s'obté en eliminar la fila $i$ i la columna $j$ de la matriu $A$. També definim $A_{ij}$ com __l'adjunt d'un element__ $a_{ij}$ d'una matriu $A$: és el seu menor complementari $\alpha_{ij}$ afectat d'un signe determinant per la seva situació en la matriu segons:


$$
\begin{pmatrix}
+ & - & +\\
- & + & -\\
+ & - & +
\end{pmatrix}
$$

Per tant, l'adjunt d'un element $a_{ij}$ d'una matriu $A$ es calcularà segons:


$$A_{ij}=\alpha_{ij}(-1)^{i+j} $$

D'aquesta manera també es pot definir la __matriu adjunta__ d'una matriu $A$, $Adj(A)$ com aquella matriu que té per elements els adjunts de cada element de la matriu original:

 $$
 Adj(A)=
 \begin{pmatrix}
 A_{11} & A_{12} & A_{13}\\
 A_{21} & A_{22} & A_{23}\\
 A_{31} & A_{32} & A_{33}
 \end{pmatrix}
$$

Així doncs, quan calculem el determinant d'una matriu desenvolupant per una fila (o una columna), estem calculant la suma de tots el productes dels elements d'una fila (o columna) multiplicada pels seus adjunts:


$$
|A|=
\begin{vmatrix}
a_{11} & a_{12} & a_{13}\\
a_{21} & a_{22} & a_{23}\\
a_{31} & a_{32} & a_{33}
\end{vmatrix}
\xrightarrow[\text{1a fila}]{} a_{11}A_{11}+a_{12}A_{12}+a_{13}A_{13}
$$

Si multipliquem els elements d'una fila (o columna) pels adjunts d'una altra fila (o columna) el valor sempre és zero.




###Determinants d'ordre 4

Sigui $A$ una matriu quadrada d'ordre 4:

$$
A=
\begin{pmatrix}
a_{11} & a_{12} & a_{13} & a_{14}\\
a_{21} & a_{22} & a_{23} & a_{24}\\
a_{31} & a_{32} & a_{33} & a_{34}\\
a_{41} & a_{42} & a_{43} & a_{44}\\
\end{pmatrix}
$$

Per calcular el seu determinant, ho farem desenvolupant per una fila o una columna:

$$
|A|=
\begin{vmatrix}
a_{11} & a_{12} & a_{13} & a_{14}\\
a_{21} & a_{22} & a_{23} & a_{24}\\
a_{31} & a_{32} & a_{33} & a_{34}\\
a_{41} & a_{42} & a_{43} & a_{44}\\
\end{vmatrix}
= a_{11}A_{11}+a_{12}A_{12}+a_{13}A_{13}+a_{14}A_{14}
$$

__Exemple 8__

Calcula el determinant següent:

$$
\begin{vmatrix}
1 & 0 & 0 & 2\\
-1 & 3 & 1 & 0\\
0 & 1 & 2 & 1\\
1 & 1 & 3 & 1\\
\end{vmatrix}
= 1 \begin{vmatrix}
3 & 1 & 0\\
1 & 2 & 1\\
1 & 3 & 1\\
\end{vmatrix}
-2 \begin{vmatrix}
-1 & 3 & 1\\
0 & 1 & 2\\
1 & 1 & 3\\
\end{vmatrix}
=1(6+1-9-1)-2(-3+6-1+2)=-11
$$

###Propietats dels determinants

1. El determinant de la matriu unitat és $1$.


    $$
    \begin{vmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    0 & 0 & 1
    \end{vmatrix}
    =1
    $$

2. El determinant d'una matriu diagonal és el producte dels elements de la diagonal principal.


    $$
    \begin{vmatrix}
    a_{11} & 0 & 0\\
    0 & a_{22} & 0\\
    0 & 0 & a_{33}
    \end{vmatrix}
    =a_{11}\cdot a_{22} \cdot a_{33}
    $$

3. El determinant d'una matriu triangular (zeros per sota o per sobre la diagonal principal) és el producte d'elements de la diagonal principal.

4. El determinant d'una matriu és igual al determinant de la seva transposta.

    $$
    \begin{vmatrix}
    a_{11} & a_{12} & a_{13}\\
    a_{21} & a_{22} & a_{23}\\
    a_{31} & a_{32} & a_{33}
    \end{vmatrix}
    =
    \begin{vmatrix}
    a_{11} & a_{21} & a_{31}\\
    a_{12} & a_{22} & a_{32}\\
    a_{13} & a_{23} & a_{33}
    \end{vmatrix}
    $$


5. El determinant d'una matriu amb dues columnes o dues files iguals és zero.

    $$
    \begin{vmatrix}
    a_{11} & a_{11} & a_{13}\\
    a_{21} & a_{21} & a_{23}\\
    a_{23} & a_{23} & a_{33}
    \end{vmatrix}
    =0
    $$

6. El determinant d'una matriu amb una columna o fila de zeros és zero.

    $$
    \begin{vmatrix}
    a_{11} & 0 & a_{13}\\
    a_{21} & 0 & a_{23}\\
    a_{31} & 0 & a_{33}
    \end{vmatrix}
    =0
    $$

7. Si tenim una matriu quadrada i intercanviem dues files (o dues columnes) el determinant esdevé el mateix però canviat de signe.

    $$
    \begin{vmatrix}
    a_{11} & a_{12} & a_{13}\\
    a_{21} & a_{22} & a_{23}\\
    a_{31} & a_{32} & a_{33}
    \end{vmatrix}
    =-
    \begin{vmatrix}
    a_{12} & a_{11} & a_{13}\\
    a_{22} & a_{21} & a_{23}\\
    a_{32} & a_{31} & a_{33}
    \end{vmatrix}
    $$

8. Si multipliquem tota una fila (o columna) d'una matriu per un mateix nombre, per calcular el determinant queda multiplicat per aquest nombre (o sigui que el podem treure factor comú a fora):


    $$
    \begin{vmatrix}
    k\cdot a_{11} & a_{12} & a_{13}\\
    k\cdot a_{21} & a_{22} & a_{23}\\
    k\cdot a_{31} & a_{32} & a_{33}
    \end{vmatrix}
    =k\cdot
    \begin{vmatrix}
    a_{11} & a_{12} & a_{13}\\
    a_{21} & a_{22} & a_{23}\\
    a_{31} & a_{32} & a_{33}
    \end{vmatrix}
    $$

9. Si sumem un mateix element a una fila (o columna) el determinant es pot separar en la suma de dos determinants (iguals) amb una de les dues files (o columnes):

    $$
    \begin{vmatrix}
    a_{11}+k_1 & a_{12} & a_{13}\\
    a_{21}+k_2 & a_{22} & a_{23}\\
    a_{31}+k_3 & a_{32} & a_{33}
    \end{vmatrix}
    =
    \begin{vmatrix}
    a_{11} & a_{12} & a_{13}\\
    a_{21} & a_{22} & a_{23}\\
    a_{31} & a_{32} & a_{33}
    \end{vmatrix}
    +
    \begin{vmatrix}
    k_1 & a_{12} & a_{13}\\
    k_2 & a_{22} & a_{23}\\
    k_3 & a_{32} & a_{33}
    \end{vmatrix}
    $$





10. Si una fila (o columna) és combinació lineal de les altres, el determinant és $0$.


     $$
     \begin{vmatrix}
     a_{11} & a_{12} & \alpha \cdot a_{11} + \beta \cdot a_{12}\\
     a_{21} & a_{22} & \alpha \cdot a_{21} + \beta \cdot a_{22}\\
     a_{31} & a_{32} & \alpha \cdot a_{31} + \beta \cdot a_{32}&
     \end{vmatrix}
     =0
     $$

11. Si a una fila (o columna) li sumem una combinació lineal de les altres dos, el determinant no varia.

     $$
     \begin{vmatrix}
     a_{11} & a_{12} & a_{13}\\
     a_{21} & a_{22} & a_{23}\\
     a_{31} & a_{32} & a_{33}
     \end{vmatrix}
     =
     \begin{vmatrix}
     a_{11} & a_{12} & a_{13}+\alpha \cdot a_{11} + \beta \cdot a_{12}\\
     a_{21} & a_{22} & a_{23}+\alpha \cdot a_{21} + \beta \cdot a_{22}\\
     a_{31} & a_{32} & a_{33}+\alpha \cdot a_{31} + \beta \cdot a_{32}&
     \end{vmatrix}
     $$


12. El determinant del producte de matrius és el producte de determinants.

     $$|A\cdot B|=|A|\cdot |B|$$


##Triangulació de Matrius

Com hem vist a les propietats, el determinant d'una matriu triangular és el producte dels elements de la seva diagonal principal. Per tant, quan hàgim de calcular un determinant d'una matriu, ens interessarà aplicar les propietats per fer la matriu triangular. Un cop tingui aquesta forma, el determinant s'obtindrà fent el producte dels elements de la diagonal principal.

Donada una matriu quadrada $4x4$, per triangular-la (zeros sota la diagonal principal) cal seguir el procediment següent:

1. Aplicant les propietats dels determinants (bàsicament operacions fila i operacions columna, amb combinacions lineals si cal) aconseguim que la primera columna tingui el primer element diferent de zero i els altres tres zero.
2. Un cop arreglada la primera columna, intentarem arreglar la segona. En aquest cas, intentarem aconseguir que els dos primers elements de la columna siguin diferents de zero i els dos següents zero.
3. Procedirem igual per la tercera columna fent que els 3 primers elements siguin diferents de zero i l'últim zero.
4. Ja hem triangulat la matriu.

Veiem-ho amb el mateix exemple anterior:

__Exemple 9__

Calcula el determinant següent triangulant la matriu primer:

$$
|A|=\begin{vmatrix}
1 & 0 & 0 & 2\\
-1 & 3 & 1 & 0\\
0 & 1 & 2 & 1\\
1 & 1 & 3 & 1\\
\end{vmatrix}
$$

1. Canviem les files 3 i 4:

    $$
    |A|=-\begin{vmatrix}
    1 & 0 & 0 & 2\\
    -1 & 3 & 1 & 0\\
    1 & 1 & 3 & 1\\
    0 & 1 & 2 & 1\\
    \end{vmatrix}
    $$

2. Ara volem aconseguir que també sigui zero l'element $a_{31}$. A la tercera fila li sumem la segona:

    $$
    |A|=-\begin{vmatrix}
    1 & 0 & 0 & 2\\
    -1 & 3 & 1 & 0\\
    0 & 4 & 4 & 1\\
    0 & 1 & 2 & 1\\
    \end{vmatrix}
    $$

3. Per aconseguir que l'element $a_{21}$ sigui zero, a la segona fila li sumem la primera:

    $$
    |A|=-\begin{vmatrix}
    1 & 0 & 0 & 2\\
    0 & 3 & 1 & 2\\
    0 & 4 & 4 & 1\\
    0 & 1 & 2 & 1\\
    \end{vmatrix}
    $$


4. Per fer l'element $a_{23}$ zero, a la segona columna li resto la tercera:

    $$
    |A|=-\begin{vmatrix}
    1 & 0 & 0 & 2\\
    0 & 2 & 1 & 2\\
    0 & 0 & 4 & 1\\
    0 & -1 & 2 & 1\\
    \end{vmatrix}
    $$

5. Per qüestions pràctiques intercanviem les files $2$ i $4$ (això provocarà un altre canvi de signe en el determinant):

   $$
   |A|=\begin{vmatrix}
   1 & 0 & 0 & 2\\
   0 & -1 & 2 & 1\\
   0 & 0 & 4 & 1\\
   0 & 2 & 1 & 2\\
   \end{vmatrix}
   $$

6. Per fer zero l'element $a_{42}$, a la quarta fila li sumem la segona multiplicada per $2$:

    $$
    |A|=\begin{vmatrix}
    1 & 0 & 0 & 2\\
    0 & -1 & 2 & 1\\
    0 & 0 & 4 & 1\\
    0 & 0 & 5 & 4\\
    \end{vmatrix}
    $$

7. Ara quasi hem acabat. Només ens falta aconseguir que l'element $a_{43}$ sigui zero. Per fer-ho, a la fila $4$ li sumem la fila $3$ multiplicada per $\frac{4}{5}$:

    $$
    |A|=\begin{vmatrix}
    1 & 0 & 0 & 2\\
    0 & -1 & 2 & 1\\
    0 & 0 & 4 & 1\\
    0 & 0 & 0 & \frac{ 11 }{ 4 }\\
    \end{vmatrix}
    $$

8. El determinant d'aquesta matriu triangular és el producte dels elements de la seva diagonal:

    $$|A|=1\cdot (-1)\cdot 4\cdot \frac{ 11 }{ 4 }=-11$$


__Nota__

S'ha d'anar molt alerta en calcular el determinant d'una matriu per triangulació. A vegades quan apliquem la propietat $11$ dels determinants l'apliquem malament: si una fila o columna li sumem una combinació lineal de les altres (o sigui, li sumem o restem les altres multiplicades per algun nombre) el determinant no varia, però si canviem aquesta fila per ella mateixa multiplicada per un nombre més una combinació lineal de les altres, el determinant es queda afectat pel nombre que l'hem multiplicat (tal i com s'explica a la propietat $8$ dels determinants).

##Matriu inversa d'una matriu quadrada

Recordem que, donada una matriu quadrada $A$ d'ordre $n$, la seva matriu inversa és aquella que multiplicada per $A$ ens dóna la matriu identitat:

$$A\cdot A^{-1}=A^{-1}\cdot A=\mathbb{1}$$

Si la matriu té determinant no nul, $|A|\ne 0$, la matriu inversa $A^{-1}$ en aquest cas es calcula segons:

$$\bbox[5px,border:2px solid black]{A^{-1}=\frac{ 1 }{ |A| }\cdot \big(Adj(A)\big)^T}$$

###Demostració###

$A$ és una matriu d'ordre $n$. Veiem quina forma té la seva matriu adjunta i la transposta de la matriu adjunta:

$$
A=\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n}\\
a_{21} & a_{22} & a_{23} &...& a_{2n}\\
a_{31} & a_{32} & a_{33} &...& a_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
a_{n1} & a_{n2} & a_{n3} &...& a_{nn}\\
\end{pmatrix}
\quad
Adj(A)=
\begin{pmatrix}
A_{11} & A_{12} & A_{13} &...& A_{1n}\\
A_{21} & A_{22} & A_{23} &...& A_{2n}\\
A_{31} & A_{32} & A_{33} &...& A_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
A_{n1} & A_{n2} & A_{n3} &...& A_{nn}\\
\end{pmatrix}
\quad
(Adj(A))^T=
\begin{pmatrix}
A_{11} & A_{21} & A_{31} &...& A_{n1}\\
A_{12} & A_{22} & A_{32} &...& A_{n2}\\
A_{13} & A_{23} & A_{33} &...& A_{n3}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
A_{1n} & A_{1n} & A_{3n} &...& A_{nn}\\
\end{pmatrix}
$$

Veiem què obtenim en multiplicar $A$ per la transposta de la seva matriu adjunta:


$$
A\cdot (Adj(A))^T=
A=\begin{pmatrix}
a_{11} & a_{12} & a_{13} &...& a_{1n}\\
a_{21} & a_{22} & a_{23} &...& a_{2n}\\
a_{31} & a_{32} & a_{33} &...& a_{3n}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
a_{n1} & a_{n2} & a_{n3} &...& a_{nn}\\
\end{pmatrix}
\cdot
\begin{pmatrix}
A_{11} & A_{21} & A_{31} &...& A_{n1}\\
A_{12} & A_{22} & A_{32} &...& A_{n2}\\
A_{13} & A_{23} & A_{33} &...& A_{n3}\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
A_{1n} & A_{1n} & A_{3n} &...& A_{nn}\\
\end{pmatrix}
=
\begin{pmatrix}
a_{11}A_{11}+a_{12}A_{12}+...+a_{1n}A_{1n} & 0 & 0 &...& 0\\
0 & a_{11}A_{11}+a_{12}A_{12}+...+a_{1n}A_{1n} & 0 &...& 0\\
0 & 0 & a_{11}A_{11}+a_{12}A_{12}+...+a_{1n}A_{1n} &...& 0\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
0 & 0 & 0 &...& a_{11}A_{11}+a_{12}A_{12}+...+a_{1n}A_{1n}\\
\end{pmatrix}
$$

Veiem que el que apareix a la diagonal de la lmatriu és el __desenvolupament del determinant de $A$__ (que és la suma dels elements de la matriu multiplicada pels seus adjunts), per tant:



$$
A\cdot (Adj(A))^T=
\begin{pmatrix}
|A| & 0 & 0 &...& 0\\
0 & |A| & 0 &...& 0\\
0 & 0 &|A|&...& 0\\
. & . & . &.& .\\
. & . & . &.& .\\
. & . & . &.& .\\
0 & 0 & 0 &...&|A|\\
\end{pmatrix}
=|A|\cdot \mathbb{1}_{nxn}
$$
on $\mathbb{1}_{nxn}$ és la matriu identitat $nxn$.
Si $|A|\ne 0$ això es pot expressar com:

$$A\cdot \frac{(Adj(A))^T}{|A|}=\mathbb{1}_{nxn}$$

i per tant, necessàriament, si multipliquem alguna cosa per $A$ i obtenim la matriu identitat, aquest factor ha de ser l'invers de la matriu $A$:

$$A^{-1}=\frac{(Adj(A))^T}{|A|}$$

__Exemple 10__

Calcula la matriu inversa de:

$$A=
\begin{pmatrix}
3 & 5 & 2\\
1 & -1 & -1\\
2 & 3 & 4
\end{pmatrix}
$$

Primer de tot haurem de comprovar si la matriu és invertible. Això vol dir essencialment que el determinant és diferent de zero:

$$|A|=
\begin{vmatrix}
3 & 5 & 2\\
1 & -1 & -1\\
2 & 3 & 4
\end{vmatrix}
=-12+6-10+4+9-20=-23\ne 0$$

Per tant és invertible. Calculem els adjunts de tots els elements per trobar la matriu adjunta i llavors calcularem la seva transposta.

$$A_{11}=
+
\begin{vmatrix}
-1 & -1\\
3 & 4
\end{vmatrix}
=-1
\qquad
A_{12}=
-
\begin{vmatrix}
1 & -1\\
2 & 4
\end{vmatrix}
=-6
\qquad
A_{13}=
+
\begin{vmatrix}
1 & -1\\
2 & 3
\end{vmatrix}
=5
$$

$$
A_{21}=
-
\begin{vmatrix}
5 & 2\\
3 & 4
\end{vmatrix}
=-14
\qquad
A_{22}=
+
\begin{vmatrix}
3 & 2\\
2 & 4
\end{vmatrix}
=8
\qquad
A_{23}=
-
\begin{vmatrix}
3 & 5\\
2 & 3
\end{vmatrix}
=1
$$

$$
A_{31}=
+
\begin{vmatrix}
5 & 2\\
-1 & -1
\end{vmatrix}
=-3
\qquad
A_{32}=
-
\begin{vmatrix}
3 & 2\\
1 & -1
\end{vmatrix}
=5
\qquad
A_{33}=
+
\begin{vmatrix}
3 & 5\\
1 & -1
\end{vmatrix}
=-8
\qquad
$$

Per tant, la matriu adjunta serà:

$$Adj(A)=
\begin{vmatrix}
-1 & -6 & 5\\
-14 & 8 & 1\\
-3 & 5 & -8
\end{vmatrix}
$$

Si la transposem obtenim:

$$(Adj(A))^T=
\begin{vmatrix}
-1 & -14 & -3\\
-6 & 8 & 5\\
5 & 1 & -8
\end{vmatrix}
$$

Així doncs, la inversa de $A$ serà:


$$A^{-1}=\frac{(Adj(A))^T}{|A|}=
\frac{ 1 }{ -23 }
\begin{pmatrix}
-1 & -14 & -3\\
-6 & 8 & 5\\
5 & 1 & -8
\end{pmatrix}
=
\begin{pmatrix}
1/23 & 14/23 & 3/23\\
6/23 & -8/23 & -5/23\\
-5/23 & -1/23 & 8/23
\end{pmatrix}
$$


##Rang d'una matriu

###Definicions

####Rang d'una matriu

Definim el rang d'una matriu com el nombre màxim de vectors fila (o vectors columna) linealment independents de la matriu.

A la pràctica vol dir quantes files o columnes no són combinació lineal de les files o columnes restants. La matriu identitat $3x3$ (tot zeros menys la diagonal amb $1$) té rang 3 perquè cap fila (o columna) és combinació lineal de les altres dues.

####Menor

Donada una matriu $A$, anomenem menor al determinant de tota matriu quadrada que es pot formar amb els elements de la matriu __respectant la distribució de files i columnes de la matriu__.

Per exemple, donada la matriu següent:

$$A=
\begin{pmatrix}
2 & 3 & -3 & 4\\
1 & 0 & 2 & 1\\
4 & 1 & 0 & 3
\end{pmatrix}
$$

Anem a veure alguns menors d'ordre 2:

$$\begin{vmatrix}
2 & 3\\
1 & 0
\end{vmatrix}
=-3
\qquad
\begin{vmatrix}
3 & 4\\
1 & 3
\end{vmatrix}
=5
\qquad
\begin{vmatrix}
2 & -3\\
1 & 2
\end{vmatrix}
=7
$$

Pel primer menor d'ordre 2 el podem orlar de dues maneres diferents i obtenim 2 menors d'ordre 3:

$$\begin{vmatrix}
2 & 3 & 4\\
1 & 0 & 1\\
4 & 1 & 3
\end{vmatrix}
=5
\qquad
\begin{vmatrix}
3 & -3 & 4\\
0 & 2 & 1\\
1 & 0 & 3
\end{vmatrix}
=7
$$

Notem que d'aquesta matriu no en podem calcular el determinant perquè no és una matriu quadrada.

#### Orlar el menor

Donat un menor d'una matriu es poden formar a partir d'ell, menors d'ordre més gran. Això es fa afegint elements d'una altra fila i una altra columna. Aquest procés s'anomena orlar el menor.

Si tornem a l'exemple anterior, i considerem el menor d'ordre 2:

$$\begin{vmatrix}
2 & 3\\
1 & 0
\end{vmatrix}
$$

El podem orlar de dues maneres, afegint-hi la fila 3 i la columna 3 o la fila 3 i la columna 4:

$$ \left|
\begin{array}{cc|c}
  2&3&-3\\
  1&0&2\\
  \hline
  4&1&0
\end{array}
\right|
\qquad
\left|
\begin{array}{cc|c}
  2&3&4\\
  1&0&1\\
  \hline
  4&1&3
\end{array}
\right|
$$

###Teorema

> El rang d'una matriu coincideix amb l'ordre més gran del menor no nul de la matriu.

En l'exemple anterior, el rang de la matriu no pot ser més gran que 3 (ja que tenim com a màxim 3 files): $Rang(A)\le 3$. Si trobem un menor d'ordre 3 no nul, podrem afirmar que el rang és 3. Si fos zero, hauríem de trobar tots els menors d'ordre 2 i mirar si són no nuls. I així seguir el procés fins a ordre 1, que de fet, si una matriu té algun element no nul, el rang com a mínim serà 1.

En l'exemple, hem trobat un menor d'ordre 3 diferent de zero:

$$ \left|
\begin{array}{cc|c}
  2&3&-3\\
  1&0&2\\
  \hline
  4&1&0
\end{array}
\right|
=17
$$

Per tant:

$$Rang(A)=3$$

Es pot demostrar també, que:

> Si tots els menors d'una matriu d'ordre $k$ són $0$, els d'ordre $k+1$ també ho són.

A la pràctica això vol dir que si tots els menors són zero, el rang serà una unitat inferior i no cal mirar els menors d'ordre superior, perquè segur que també seran zero.

Si utilitzant totes les possibilitats d'orlar un menor fem servir la mateixa fila però diferents columnes (o al revés) i veiem que tots els determinants són zero, podem afirmar que la fila (o columna) amb la que hem orlat el menor és combinació lineal de les files (o columnes) del menor. Veurem això amb més claredat a l'exemple 11.

###Mètode per calcular el rang

1. Si la matriu té un element diferent de $0$ el rang serà com a mínim 1.
2. A continuació orlem aquest menor d'ordre 1 fins a trobar un menor d'ordre 2 diferent de zero. En aquest cas, podem afirmar que el rang com a mínim és 2. Si tots els d'ordre 2 són zero, el rang de la matriu és 1 i ja hauríem acabat.
3. En general, si trobem menors no nuls, continuem aquest procés fins a trobar un menor d'ordre $k$ tal que al orlar-lo amb les files i columnes que queden tots els menors d'ordre $k+1$ són nuls. Aleshores el rang de la matriu $A$ serà $k$.


__Exemple 11__

Trobeu el rang de la matriu:

$$
A=
\begin{pmatrix}
2 & -2 & -8 & -1 & 1\\
2 & 2 & 3 & 1 & 0\\
12 & 8 & 7 & 4 & 1\\
8 & 4 & 1 & 2 & 1
\end{pmatrix}
$$

Menors d'ordre 1:

$$|2|\ne 0$$

El rang com a mínim és 1. Trobem ara un menor d'ordre 2 no nul:

$$
\begin{vmatrix}
2 & -2\\
2 & 2
\end{vmatrix}
=8
$$

Per tant, el rang com a mínim és 2.

Anem a orlar aquest menor de totes les maneres possibles. Comencem pels elements de la fila 3:

$$ \left|
\begin{array}{cc|c}
  2&2-&-8\\
  2&2&3\\
  \hline
  12&8&7
\end{array}
\right|
=0
\qquad
\left|
\begin{array}{cc|c}
  2&-2&-1\\
  2&2&1\\
  \hline
  12&8&4
\end{array}
\right|
=0
\left|
\begin{array}{cc|c}
  2&-2&1\\
  2&2&0\\
  \hline
  12&8&1
\end{array}
\right|
=0
$$

Hem orlat el menor d'ordre 2 sempre amb la fila 3 canviant les columnes i veiem que tots són zero. Per tant, podem afirmar que la fila 3 és una combinació lineal de les files 1 i 2.

Si orléssim el menor de la mateixa manera que hem fet però amb els elements de la fila 4, veuríem que també són zero i per tant, podem afirmar que la fila 4 és també combinació lineal de les files 1 i 2. Com que no hi ha cap altre menor orlat d'ordre 3, podem afirmar que el rang de la matriu és 2.
