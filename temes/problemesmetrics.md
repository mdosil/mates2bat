#Tema 9: Problemes mètrics


##Distància entre dos punts

Tal i com vèiem [el curs passat](http://mdosil.cat/mates1batcientific/temes/rectes/#distancia-entre-dos-punts), la distància entre 2 punts $A(a_1,a_2,a_3)$ i $B(b_1,b_2,b_3)$ a $\mathbb{ R }^3$ és el mòdul del vector format per aquests punts:

$$d(A,B)=|\sqrt{ (b_1-a_1)^2+ (b_2-a_2)^2+(b_3-a_3)^2}|$$

##Distància d'un punt a una recta

Donat un punt $P(a,b,c)$ i una recta $r$ qualsevol, la distància d'aquest punt a la recta s'obté calculant __la projecció ortogonal del punt $P$ sobre la recta $r$, el punt $P^\prime$__. La distància serà el mòdul del vector $\overrightarrow{ P^{\prime}P }$.

<iframe scrolling="no" title="distancia punt - recta R3" src="https://www.geogebra.org/material/iframe/id/dyat7TWz/width/700/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="700px" height="719px" style="border:0px;"> </iframe>

Aquesta distància es pot calcular de moltes maneres. Ho farem amb un exemple concret i el resoldrem de 3 maneres completament diferents.

__Exemple 1__

Troba la distància del punt $P(5,6,1)$ a la recta $r:\frac{ x }{ 1 }=\frac{ y-1 }{ 1 }=\frac{ z+1 }{ 4 }$.

1. Expressem la recta amb l'equació paramètrica, escrivim la projecció $P^\prime$ en funció del paràmetre i exigim que el vector $\overrightarrow{ P^{\prime}P}$ sigui perpendicular al vector director de la recta, $\overrightarrow{ v }$.

    La recta que ens donen en forma paramètrica és:

    $$r: \begin{cases} x&=\lambda \\ y&=1+\lambda \\ z&=-1+4\lambda  \end{cases}$$

    Per tant, qualsevol punt de la recta $r$, i $P^{\prime}$ en particular, tindrà la forma:

    $$P^{\prime}=(\lambda,1+\lambda,-1+4\lambda)$$

    Si calculem ara la distància entre $P$ i $P^{\prime}$ a través del mòdul del vector $|\overrightarrow{ P^{\prime}P}|$, tenim que:

    $$\overrightarrow{ P^{\prime}P}=(5-\lambda,6-1-\lambda,1+1-4\lambda)=(5-\lambda,5-\lambda,2-4\lambda)$$

    Alhora, aquest vector és perpendicular al vector director de la recta, $\overrightarrow{ v }=(1,1,4)$. Per tant, el seu producte escalar serà zero:

    $$\overrightarrow{ v }\cdot \overrightarrow{ P^{\prime}P }=1(5-\lambda)+1(5-\lambda)+4(2-4\lambda)=0 \rightarrow \lambda = 1$$

    Per tant, la projecció de $P$ sobre la recta $r$ és: $\overrightarrow{ P^{\prime}}=(1,2,3)$ i la distància del punt a la recta és:


    $$d(P,r)=|\overrightarrow{ P^{\prime}P}|=\sqrt{ (5-1)^2+(6-2)^2+(3-1)^2 }=6$$


2. Calculem l'equació del pla $\pi$ perpendicular a $r$ que passa per $P$. La intersecció entre la recta i el pla serà necessàriament el punt $P^{\prime}$, la projecció de $P$ sobre la recta $r$.


    <iframe scrolling="no" title="distancia punt - recta R3 v2" src="https://www.geogebra.org/material/iframe/id/s99Nr2rE/width/700/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="700px" height="719px" style="border:0px;"> </iframe>


    El pla $\pi$ perpendicular a $r$ tindrà de vector normal el vector director de la recta: $\overrightarrow{ n }=(1,1,4)$. Per tant, serà de la forma: $\pi: x+y+4z+D=0$. Com que el punt $P(5,6,1)$ pertany al pla, tenim que:

    $$5+6+4\cdot 1+D=0\rightarrow D=-15$$

    L'equació del pla és doncs: $\pi: x+y+4z-15=0$

    Si substituïm les coordenades $x$, $y$ i $z$ en funció de $\lambda$ a l'equació del pla i aïllem $\lambda$ trobarem les coordenades del punt $P^{\prime}$:

    $$\lambda+1+\lambda+4(-1+4\lambda)-15=0\rightarrow \lambda=1\rightarrow P^{\prime}=(1,2,3)$$

    A partir d'aquí, calculem la distància igual que ho hem fet a l'apartat anterior.


3. Calculem la distància aplicant la fòrmula de la distància d'un punt $P$ a una recta $r$.

    <iframe scrolling="no" title="Distancia punt recta producte vectorial R3" src="https://www.geogebra.org/material/iframe/id/S8BgeP7Y/width/700/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="700px" height="719px" style="border:0px;"> </iframe>

    Donat un punt $Q$ de la recta qualsevol, mirant el dibuix i aplicant la trigonometria, la distància entre $P$ i $P^{\prime}$, es pot calcular com:

    $$d(P,r)=|\overrightarrow{ P^{\prime}P }|=|\overrightarrow{ PQ }|\cdot \sin (\alpha) $$

    Si multipliquem i dividim l'expressió anterior pel mòdul del vector director de la recta, $|\overrightarrow{ v }|$ obtenim:


    $$d(P,r)=|\overrightarrow{ P^{\prime}P }|=\frac{|\overrightarrow{ PQ }|\cdot \sin (\alpha) \cdot |\overrightarrow{ v }|}{\overrightarrow{ v }}$$

    Si ens fixem, el numerador és el mòdul del producte vectorial dels vectors $\overrightarrow{ PQ }$ i $\overrightarrow{ v }$. Per tant, podem reescriure aquesta fòrmula de la manera següent:

    $$\bbox[5px,border:2px solid black]{d(P,r)=\frac{ |\overrightarrow{ PQ }\times \overrightarrow{ v }| }{ |\overrightarrow{ v }| }}$$

    Si apliquem la fòrmula en el nostre problema concret:

    $$P=(5,6,1),\qquad Q=(0,1,-1)\rightarrow \overrightarrow{ PQ }=(-5,-5,-2)$$

    Hem agafat com a punt $Q$ el punt de l'equació contínua de la recta.

    Aplicant ara la fòrmula:


    $$d(P,r)=\frac{ |\overrightarrow{ PQ }\times \overrightarrow{ v }| }{ |\overrightarrow{ v }| }=\frac{ | (-5,-5,-2) \times (1,1,4)| }{ |(1,1,4)| }=\frac{ |(-18,18,0)| }{ \sqrt{1+1+16} }=\frac{ \sqrt{18^2+18^2} }{ \sqrt{18} }=6$$

##Distància d'un punt a un pla

Per calcular la distància d'un punt $P$ a un pla, cal fer un procediment igual a la manera 2 de l'exemple 1 anterior:

1. Primer caldrà trobar la recta perpendicular al pla que passa pel punt $P$ en qüestió. Per això agafem com a vector director de la recta el vector normal del pla. Com a punt de la recta agafem el punt $P$ i trobem l'equació.

2. Un cop tenim l'equació de la recta, la projecció del punt $P$ sobre el pla, $P^{\prime}$, és la intersecció de la recta amb el pla.
3. La distància entre $P$ i el pla és el mòdul del vector $|\overrightarrow{ P^{\prime}P }|$


##Punt simètric d'un punt respecte una recta o un pla

Un cop hem trobat la projecció d'un punt $P$ sobre una recta o un pla, el punt $P^\prime$, considerem ara el punt simètric al punt $P$, $P ^{\prime \prime}$ com aquell que el punt mig del segment $\overline{ PP^{\prime \prime} }$ és $P^\prime$. Això ho veurem més clar en un dibuix:

<iframe scrolling="no" title="Punt simètric respecte una recta a R3" src="https://www.geogebra.org/material/iframe/id/eBAWZSP2/width/700/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="700px" height="719px" style="border:0px;"> </iframe>

Per tant, per trobar el punt simètric respecte una recta o pla, primer caldrà trobar la projecció ortogonal del punt respecte la recta o pla i després aplicar [la fòrmula del punt mig d'un segment](http://mdosil.cat/mates1batcientific/temes/vectors/#calcul-del-punt-mig-dun-segment). Si assumim que $P=(x,y,z)$, $P^{\prime}=(x^\prime , y^\prime , z^ {\prime} )$ i $P^{\prime \prime}=(x^{\prime \prime} , y^{\prime \prime} , z^ {\prime \prime} )$, es compleix que:

$$(x^\prime , y^\prime , z^ {\prime} )=(\frac{ x+x^{\prime \prime} }{ 2 },\frac{ y+y^{\prime \prime} }{ 2 }, \frac{ z+z^{\prime \prime} }{ 2 })$$

##Distància entre dues rectes

Si les dues rectes es tallen, la distància serà zero. Aquest cas només té sentit plantejar-lo per dues rectes que són paral.leles o es creuen. Per tant, primer caldrà estudiar [la posició relativa entre les dues rectes](http://mdosil.cat/mates2batcientific/temes/equacionsrectesplans/#posicio-relativa-de-dues-rectes) per determinar el que s'ha de fer després. Ho veurem tot a través d'un exemple.

__Exemple 2__

Troba la distància entre les rectes $r:\frac{ x-1 }{ 2 }=\frac{ y }{ 1 }=\frac{ z-2 }{ 0 }$ i $s:\frac{ x }{ 1 }=\frac{ y }{ 1 }=\frac{ z -1 }{ 1 }$.

1. Posició relativa de les dues rectes

    Agafem els 2 vectors directors de $r$ i $s$, $\overrightarrow{ u }=(2,1,0)$ i $\overrightarrow{ v }=(1,1,1)$. Juntament amb un punt de $r$, $P=(1,0,2)$ i un punt de $s$, $Q=(0,0,1)$, creem el vector $\overrightarrow{ PQ }=(-1,0,-1)$. Amb aquests 3 vectors, mirem quin és el determinant de la matriu $3x3$. Si aquest determinant és diferent de zero, voldrà dir que el rang és 3 i les rectes es creuen:


    $$\begin{vmatrix}
    -1 & 2 & 1 \\
    0 & 1 & 1\\
    -1 & 0 & 1
    \end{vmatrix}=-2
    $$

    Per tant, les rectes es creuen.

2. Considerem la recta $t$ perpendicular a $r$ i a $s$.

    Aquesta recta tindrà de vector director $\overrightarrow{ w }$ que serà perpendicular alhora a $\overrightarrow{ u }$ i a $\overrightarrow{ v }$:

    $$\overrightarrow{ w }=\begin{vmatrix}
    i & j & k \\
    2 & 1 & 0\\
    1 & 1 & 1
    \end{vmatrix}=(1,-2,1)
    $$

3. Trobem l'equació del pla $\pi$ que conté la recta $t$ i la recta $s$

     Tenim 2 vectors que pertanyen en aquest pla, el vector $\overrightarrow{ w }$ de $t$ i el vector $\overrightarrow{ v }$ de $s$. Només ens falta agafar un punt del pla per trobar-ne l'equació. Com a punt del pla podem agafar el punt $Q=(0,0,1)$ de $s$. Per tant, el pla tindrà com a equació:


     $$\begin{vmatrix}
     x-0 & 1 & 1 \\
     y-0 & -2 & 1\\
     z-1 & 1 & 1
     \end{vmatrix}=0 \rightarrow -3x+3z-3=0 \rightarrow x-z+1=0
     $$

4. Busquem la intersecció del pla $\pi$ amb la primera recta, $r$. Això ens donarà un punt, diguem-li $A$.

    Expressem l'equació de $r$ de forma paramètrica i substituïm els valors de $x$, $y$ i $z$ en l'equació del pla:

    $$r: \begin{cases} x&=1+2\lambda \\ y&=\lambda \\ z&=2  \end{cases}\rightarrow (1+2\lambda)-2+1=0 \rightarrow \lambda=0$$

    Per tant, substituïnt el valor de $\lambda$ a l'equació paramètrica de $r$ trobem que el punt $A$ té coordenades:

    $$A=(1,0,2)$$

    Que casualment coincideix amb $P$.


5. Trobem l'equació de la recta $t$:

     $$\frac{ x-1 }{ 1 }=\frac{ y-0 }{ -2 }= \frac{ z-2 }{ 1 }$$


6. La distància entre les rectes $r$ i $s$ és la distància de $A$ a la recta $s$:

     $$d(r,s)=d(P,s)=\frac{ |\overrightarrow{ PQ }\times \overrightarrow{ v }| }{ |\overrightarrow{ v }| }=\frac{ |(-1,0,-1)\times (1,1,1)| }{ \sqrt{ 1+1+1 }}=\frac{ \sqrt{ 6 }}{ 3 }u \approx 0.82 $$


7. Representació gràfica.

    A sota trobem la representació gràfica del problema. En blau hi ha representades les rectes $r$ i $s$ originals, en taronja la recta $t$ perpendicular a totes dues. També hi ha representat el pla $\pi$ en color blau.

   <iframe scrolling="no" title="Distancia entre dues rectes que es creuen R3" src="https://www.geogebra.org/material/iframe/id/RaMPpn5T/width/700/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="700px" height="719px" style="border:0px;"> </iframe>


Existeix també una fòrmula per a calcular la distància entre dues rectes que es creuen. Donades dues rectes $r$ i $s$ de vectors directors $\overrightarrow{ u }$ i $\overrightarrow{ v }$ respectivament, amb punts $P$ de $r$ i $Q$ de $s$, la distància entre les dues rectes es pot trobar amb l'expressió següent:

$$d(r,s)=\frac{ |\overrightarrow{ PQ } \cdot (\overrightarrow{ u }\times \overrightarrow{ v })|}{ |\overrightarrow{ u }\times \overrightarrow{ v }| }$$

*Manera 2*

També podíem haver fet aquest problema d'una altra manera. Anem a veure-ho a sota.

1. Trobem l'equació d'un pla $\pi$ que conté la recta de sota, $s$ i és paral.lel a la recta de dalt, $r$. Per trobar-lo, com que les dues rectes ja hem comprovat prèviament que es creuen, agafo els 2 vectors directors de $r$ i $s$ i el punt $Q$ de $s$:


    $$\begin{vmatrix}
    x-0 & 2 & 1 \\
    y-0 & 1 & 1\\
    z-1 & 0 & 1
    \end{vmatrix}=0 \rightarrow x-2y+z-1=0
    $$

2. Per trobar la distància entre $r$ i $s$ nomes ens cal trobar la distància entre $P$ i la seva projecció ortogonal sobre el pla $\pi$, $P^{\prime}$. Per fer-ho, calculem la recta perpendicular al pla $\pi$ que passa per $P$, $t$. Aquesta tindrà vector director $\overrightarrow{ w }=\overrightarrow{ n }=(1,-2,1)$:


    $$
    t:\begin{cases} x=1+\lambda  \\ y=-2 \lambda \\ z= 2+ \lambda  \end{cases}
    $$

3. El punt $P^{\prime}$ serà la intersecció entre $t$ i el pla $\pi$. Qualsevol punt de $t$ té la forma: $P^{\prime}=(1+\lambda,-2\lambda,2+\lambda)$. Si ho substituïm a l'equació de $\pi$:

    $$(1+\lambda)-2(-2\lambda)+(2+\lambda)-1=0\rightarrow \lambda=-\frac{ 1 }{ 3 }$$


4. La distància entre les dues rectes serà el mòdul del vector $\overrightarrow{ PP^{\prime} }$:


    $$P^{\prime}=\big( \frac{ 2 }{ 3 },\frac{ 2 }{ 3 },\frac{ 5 }{ 3 } \big) \rightarrow |\overrightarrow{ P P^{\prime} }|=\sqrt{ (\frac{ 2 }{ 3 }-1)^2+ (\frac{ 2 }{ 3 }-0)^2 + (\frac{ 5 }{ 3 }-2)^2 }=\frac{ \sqrt{ 6} }{ 3 }$$

##Distància d'una recta a un pla

Si la recta i el pla es tallen, o la recta està dins el pla, llavors la distància també serà zero. Per tant, primer caldrà trobar [la posició relativa](http://mdosil.cat/mates2batcientific/temes/equacionsrectesplans/#posicio-relativa-entre-rectes-i-plans) entre la recta i el pla.

Si són paral.lels no coincidents, l'únic que haurem de fer és agafar un punt de la recta i calcular [la distància del punt al pla donat](http://mdosil.cat/mates2batcientific/temes/problemesmetrics/#distancia-dun-punt-a-un-pla).

###Projecció d'una recta sobre un pla

Donat un pla $\pi$ i una recta $r$ qualsevol, es pot calcular la seva projecció sobre el pla. Diguem que és com si calculéssim l'ombra de la recta sobre el pla. Ho veurem a través d'un exemple.

__Exemple 3__

Calcula la projecció de la recta $r:\begin{cases} x=-4+6\lambda  \\ y=3  \\ z= 5-5 \lambda  \end{cases}$ sobre el pla $\pi: z=3$.

Primer de tot cal comprovar la posició relativa entre la recta i el pla. El vector director de la recta és $\overrightarrow{ v }=(6,0,-5)$ i el vector normal del pla és $\overrightarrow{ n }=(0,0,1)$. Veiem que no són perpendiculars, per tant, la recta i el pla es tallen.

Per calcular la projecció de la recta sobre el pla, primer de tot calcularem la projecció d'un punt $P$ de la recta sobre el pla, $P^{\prime}$. Llavors, calcularem el punt de tall de la recta $r$ amb el pla $\pi$. Amb aquests 2 punts, ja en tindrem prou per trobar la projecció de la recta $r$ sobre el pla $\pi$, $r^{\prime}$.

L'equació de la recta $t$ que és perpendicular a $\pi$ i passa per $P$ té vector director $\overrightarrow{ n }$ i és:

$t:\begin{cases} x=-4  \\ y=3  \\ z= 5+ \lambda  \end{cases}$

Per trobar $P^\prime$ només ens cal trobar la intersecció de $t$ amb $\pi$:

$$5+\lambda=3\rightarrow \lambda=-2 \rightarrow P^{\prime}=(-4,3,3)$$.

Ara trobarem el punt $C$ d'intersecció de $r$ amb el pla $\pi$ i tindrem el segon punt. Si substituïm l'equació paramètrica de $r$ a l'equació del pla obtenim:

$$5-5\lambda=3\rightarrow \lambda=\frac{ 2 }{ 5 }\rightarrow C=(-\frac{ 8 }{ 5 },3,3)$$

Llavors, l'equació de la projecció de $r$ sobre el pla $\pi$, o sigui $r^\prime$ la podem trobar amb els punts $P^{\prime}=(-4,3,3)$ i C=(-\frac{ 8 }{ 5 },3,3)$$. Calculeu el seu vector director:

$$\overrightarrow{ v^\prime }=\overrightarrow{ P^\prime C} =(-\frac{ 12 }{ 5 },0,0)$$

Per tant, l'equació de la recta és:

$r^\prime:\begin{cases} x=-4-\frac{ 12 }{ 5 }\lambda  \\ y=3  \\ z= 3  \end{cases}$


<iframe scrolling="no" title="Projeccio recta sobre pla R3" src="https://www.geogebra.org/material/iframe/id/bkb2ztfK/width/700/height/719/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="700px" height="719px" style="border:0px;"> </iframe>

##Distància entre dos plans

Aquí funcionarà una mica igual. Caldrà primer estudiar-ne [la seva posició relativa](http://mdosil.cat/mates2batcientific/temes/equacionsrectesplans/#posicio-relativa-entre-plans). Si els plans són coincidents o es tallen, la distància serà zero. Si els plans són paral.lels, s'agafarà un punt qualsevol d'un dels plans i es calcularà la distància d'aquest punt a l'altre pla.
