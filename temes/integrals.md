#Tema 4: Integrals

##Integrals indefinides

###Primitiva d'una funció

Direm que $F(x)$ és una __primitiva__ de $f(x)$ si:

$$
\bbox[5px,border:2px solid black] {F^\prime (x)=f(x) }
$$

__Exemple 1__

Dóna alguna de les primitives de $f(x)=x^2$.

Caldrà buscar una funció $F(x)$ tal que derivant-la ens doni la funció $x^2$. En principi veiem que haurà de ser un polinomi de grau 3:

\begin{align}
F(x)&=\frac{x^3}{3} \mbox{ és una primitiva de } f(x) \mbox{, però}\\
F(x)&=\frac{x^3}{3}+5 \mbox{ també ho és}
\end{align}

Ambdues de les funcions anteriors quan les derivem obtenim $f(x)=x^2$.

Podem afirmar també que:

> Totes les primitives d'una funció difereixen només en una constant.

###Definició: Integral indefinida

Es defineix la integral indefinida d'una funció com el conjunt de totes les primitives d'aquesta funció i es representa de la manera següent:

$$
\bbox[5px,border:2px solid black] {\int f(x) \cdot dx = F(x)+C }
$$

on $C$ és una constant.

###Taula d'integrals indefinides immediates

Amb això podem establir una llista d'integrals indefinides immediates, per les funcions més senzilles:

| Funció     | Integral |
| :------------- |:------------- |
| Polinòmica     |$$\int x^n dx=\frac{x^{n+1}}{n+1}+C$$|
| Exponencial     |$$\int e^x dx=e^x+C$$|
| Inversa     |$$\int \frac{1}{x} dx=\ln (x)+C$$|
| Cosinus     |$$\int \cos x dx= \sin x+C$$|
| Sinus     |$$\int \sin x dx= -\cos x+C$$|
| Inversa del cosinus al quadrat     |$$\int \frac{1}{(\cos x)^2} dx= \tan x+C$$|
| Funció racional inversa de trigonomètrica    |$$\int \frac{1}{1+x^2} dx= \tan^{-1} x+C$$|
| Funció racional inversa de trigonomètrica    |$$\int \frac{1}{\sqrt{1-x^2}} dx= \sin^{-1} x+C$$|

__Exemple 2__

Anem a calcular $\int \frac{1}{2x} dx$. Tal i com hem vist a dalt, totes les primitives d'una funció difereixen en una constant. Però aquí sembla que no es compleixi aquesta regla. Podem integrar aquesta funció de dues maneres diferents:

\begin{align}
\int \frac{1}{2x} dx =
\begin{cases} \frac{1}{2}\int 2 \frac{1}{2x}dx = \frac{1}{2} \ln (2x)+C\\
\frac{1}{2} \int \frac{1}{x} dx=\frac{1}{2} \ln x +C
    \end{cases}
    \end{align}

Semblaria que les dues funcions són diferents i que hi hauria dues primitives per a la mateixa funció. Però veiem que són la mateixa i només difereixen en una constant. Aplicant les lleis dels logaritmes a la primera expressió tenim que:

$$\frac{1}{2} \ln (2x)+C=\frac{1}{2}(\ln 2 + \ln x)+C=\frac{\ln 2}{2}+ \frac{1}{2} \ln x +C = \frac{1}{2} \ln x + C^\prime$$

ja que $\ln 2$ és un nombre real. Per tant, acabem de veure que les dues primitives són la mateixa i només difereixen en una constant.


###Taula d'algunes integrals indefinides quasi-immediates


Considerem $u(x)$ una funció qualsevol. Llavors:


|      | |
| :------------- |:------------- |
|    $$\int \frac{1}{u(x)}\cdot u^\prime (x) dx=\ln(x)+C$$  | |
|    $$\int e^{u(x)}\cdot u^\prime (x) dx=e^{u(x)}+C$$  | |
|    $$\int u(x)^n \cdot u^\prime (x) dx= \frac{u(x)^{n+1}}{n+1}+C$$  | |
|    $$\int \cos(u(x))\cdot u^\prime (x) dx=\sin(u(x))+C$$  | |
|    $$\int \sin(u(x))\cdot u^\prime (x) dx=-\cos(u(x))+C$$  | |
|    $$\int \frac{1}{\cos(u(x))^2}\cdot u^\prime (x) dx=\tan(u(x))+C$$  | |
|    $$\int \frac{1}{1+u(x)^2}\cdot u^\prime (x) dx=\tan^{-1}(u(x))+C$$  | |
|    $$\int \frac{1}{\sqrt{1-u(x)^2}}\cdot u^\prime (x) dx=\sin^{-1}(u(x))+C$$  | |



###Propietats de les integrals indefinides

Es pot demostrar que les integrals indefinides compleixen:


1. $\int (f(x)+g(x)) \cdot dx = \int f(x)dx+\int g(x)dx $
2. $\int k \cdot f(x) \cdot dx = k \cdot \int f(x)dx , k \in \mathbb{R} $

###Més exemples d'integrals indefinides quasi-immediates

__Exemple 3__

$$\int \cot x dx=\int \frac{\cos x}{\sin x}dx=\int \frac{1}{\sin x}\cdot \cos x dx=\ln (\sin x) + C$$


__Exemple 4__

$$\int \tan x dx=\int \frac{\sin x}{\cos x}dx= -\int \frac{1}{\cos x}\cdot (-\sin x) dx=-\ln (\cos x) + C$$

__Exemple 5__

$$\int \frac{x}{3x^2+5} dx=\frac{1}{6} \int \frac{6x}{3x^2+5} dx = \frac{1}{6} \ln(3x^2+5) + C$$

__Exemple 6__

$$\int x \sqrt[3]{3x^2+1}dx=\int x (3x^2+1)^{\frac{1}{3}}dx=\frac{1}{6} \int 6x (3x^2+1)^\frac{1}{3} dx= \frac{1}{6}\cdot \frac{3(3x^2+1)^{\frac{4}{3}}}{4} + C=...=\frac{1}{8} \cdot (3x^2+1) \sqrt[3]{3x^2+1}+C$$

__Exemple 7__

$$\int \frac{\ln x}{x} dx=\int \ln x \cdot \frac{1}{x} dx=\frac{\ln^2 x}{2}+C$$






##Mètodes d'integració
A continuació explicarem algunes mètodes d'integració comuns depenent del tipus de funció que vulguem integrar.

###Integració de funcions racionals

Entenem com a funció racional una funció del tipus $R(x)=\frac{P(x)}{Q(x)}$ on $P$ i $Q$ són polinomis.

####Integrals racionals quasi immediates
Hi ha algunes integrals racionals que són quasi immediates i que no cal aplicar cap mètode per trobar-ne la primitiva. Ho il.lustrarem amb uns quants exemples.

__Exemple 8__

Aquesta integral racional amb $n>1$ es pot tractar com una integral polinòmica amb exponent negatiu:

$$\int \frac{dx}{(x-a)^n}=\int (x-a)^{-n} dx=\frac{(x-a)^{-n+1}}{-n+1}  + C=\frac{1}{(1-n)(x-a)^{n-1}}+C$$

__Exemple 9__

Aquesta és una generalització d'integral del tipus $\tan^{-1}$. Considerant $b>0$ i $c>0$:

$$\int \frac{1}{b+cx^2} dx=\int \frac{\frac{1}{b}}{1+\frac{cx^2}{b}}dx=\frac{1}{b}\int \frac{1}{1+(\frac{\sqrt{c}x}{\sqrt{b}})^2}dx=\frac{1}{b}\frac{\sqrt{b}}{\sqrt{c}}\int \frac{\frac{\sqrt{c}}{\sqrt{b}}}{1+(\frac{\sqrt{c}x}{\sqrt{b}})^2}dx=\frac{1}{\sqrt{bc}} tan ^{-1}(\frac{\sqrt{c}x}{\sqrt{b}})+C$$

__Exemple 10__

La integral següent il.lustra el cas en que el grau del numerador i el del denominador és 1. Aquest tipus d'integrals les dividirem en dues parts, en una la integració serà la d'una constant i a la segona part, obtindrem un logaritme:

$$\int \frac{x+2}{x-3} dx=\int \frac{x-3+3+2}{x-3} dx = \int \frac{x-3}{x-3} dx+ \int \frac{5}{x-3} dx = \int 1 dx+ \int \frac{5}{x-3} dx =x+5\ln(x-3)+C$$


__Exemple 11__

En aquest exemple tenim una funció racional on el grau del denominador és $2$ i el grau del numerador $1$, de tal manera que podem transformar el numerador com a derivada del denominador i obtenir un logaritme:

$$\int \frac{x^2-2x}{x^3-3x^2+1} dx=\frac{1}{3}\int \frac{3x^2-6x}{x^3-3x^2+1} dx = \frac{1}{3}\ln(x^3-3x^2+1)+C$$

####Integrals racionals amb el grau del numerador més gran que el grau del denominador (fraccions impròpies)

Si en una fracció algebraica $\frac{P(x)}{Q(x)}$ el grau de $P$ és major que el grau de $Q$ diem que la fracció és __impròpia__. Per a integrar una expressió d'aquest tipus ens caldrà transformar-la primer en una fracció on el grau de $P$ sigui més petit que el de $Q$ (fracció __pròpia__). Per a fer-ho, recordem la divisió de polinomis i la seva prova. Donats dos polinomis $P(x)$ i $Q(x)$ la seva divisió dóna un quocient $S(x)$ i un reste $R(x)$. Llavors sempre es compleix que:

\begin{align}
P(x)=S(x)Q(x)+R(x)\\
\frac{P(x)}{Q(x)}=S(x)+\frac{R(x)}{Q(x)}
\end{align}

i si grau $P(x)>$ grau $Q(x)$ llavors sempre es compleix que grau $R(x)>$ grau $Q(x)$. Això és el que haurem de fer abans d'integrar una fracció algebraica amb grau del numerador més gran que el grau de denominador. Anem a veure'n un exemple.

__Exemple 12__


$$\int \frac{x^3-4}{x^2-x-2}dx$$

Com que és una fracció impròpia, fem la divisió de polinomis i calculem el quocient i el reste. Aplicant l'expressió anterior obtenim que:

$$\frac{x^3-4}{x^2-x-2}=(x+1)+\frac{3x-2}{x^2-x-2}$$

Per tant:

$$\int \frac{x^3-4}{x^2-x-2}dx=\int (x+1)dx+ \int \frac{3x-2}{x^2-x-2} dx= \frac{x^2}{2}+x+\int \frac{3x-2}{x^2-x-2} dx$$

Per calcular la última integral, ens caldrà passar a l'apartat següent.



####Integrals racionals amb el grau del numerador més petit que el grau del denominador (fraccions pròpies)

Treballarem amb l'exemple anterior per explicar-ho.

Volem calcular $\int \frac{3x-2}{x^2-x-2}dx$

El que farem és descomposar el denominador en factors i expressar la fracció anterior com una suma de dues fraccions algebraiques on el denominador és un polinomi de grau 1. Si busquem les arrels de $x^2-x-2$ veiem que són $2$ i $-1$. Per tant:


$$\frac{3x-2}{x^2-x-2}=\frac{3x-2}{(x+1)(x-2)}$$

#####Expansió en fraccions parcials

Primer comprovarem que el numerador no sigui la derivada del denominador (o que quasi ho sigui i només hi falti multiplicar per un nombre com a l'exemple 11). Si fos així, ja hauríem acabat.

En cas contrari, expressarem aquesta fracció com a suma de fraccions parcials. Aquest mètode és útil per descomposar una fracció algebraica com a suma de fraccions on el numerador té grau $0$ i el denominador grau $1$. El resultat de la integral esdevé una suma de logaritmes.

Si tenim en compte l'exemple anterior:



$$\frac{3x-2}{(x+1)(x-2)}=\frac{A}{x-2}+\frac{B}{x+1}$$

I si ho multipliquem tot per $(x+1)(x-2)$ tenim que:

$$3x-2=A(x+1)+B(x-2)$$


Per trobar les constants $A$ i $B$ substituïm $x$ per dos valors fàcils de trobar i resolem el sistema:



$$\left.\begin{aligned}
x=2&\rightarrow 6-2=3A+0B \\
x=-1&\rightarrow -3-2=0A-3B
\end{aligned}\right\rbrace$$

La solució del sistema és $A=\frac{4}{3}$ i $B=\frac{5}{3}$.

Per tant, tenim que:

$$\frac{3x-2}{(x+1)(x-2)}=\frac{\frac{4}{3}}{x-2}+\frac{\frac{5}{3}}{x+1}$$

I això ens permet calcular la nostra integral com a suma d'integrals quasi immediates:


$$\int \frac{3x-2}{x^2-x-2}dx=\frac{4}{3}\int \frac{1}{x-2}dx+\frac{5}{3}\int \frac{1}{x+1}dx=-\frac{4}{3} \ln (x-2)+\frac{5}{3} \ln (x+1)+C$$

Per tant, la integral que volíem calcular al principi en donarà:

$$\int \frac{x^3-4}{x^2-x-2}dx = \frac{1}{2}x^2+x+\frac{4}{3} \ln(x-2) + \frac{5}{3} \ln(x+1)+C$$

En general, per l'expansió en fraccions parcials d'una fracció pròpia, seguirem les normes següents:

1. Per cada factor lineal del denominador, utilitzarem una constant dividit per aquest factor i una altra constant dividida per una potència d'aquest factor si aquest es repeteix (arrels múltiples)
2. Per cada factor quadràtic irreductible del denominador (com per exemple $x^2+1$), utilitzarem un terme lineal dividit per aquest factor i un altre per si el factor es repeteix.

Alguns exemples:

\begin{align}
\frac{1}{(x+1)(x^2+2)}&=\frac{A}{x+1}+\frac{Bx+C}{x^2+2}\\
\frac{x^2-4}{x^2(x^2+1)^2}&=\frac{A}{x}+\frac{B}{x^2}+\frac{Cx+D}{x^2+1}+\frac{Ex+F}{(x^2+1)^2}\\
\end{align}



#####Completant quadrats

Donada una fracció on el grau del numerador és $0$ i el del denominador és grau $2$, si el polinomi del denominador __no té arrels reals__ intentarem expressar el denominador com a un terme quadràtic més una constant i així obtindrem una integral del tipus $tan^{-1}$. Anem a veure un exemple:

__Exemple 13__

$$\int \frac{1}{4x^2-4x+5} dx$$

Transformem d'aquesta manera el denominador:

\begin{align}
4x^2-4x+5&=4(x^2-x)+5\\
&=4(x^2-x+\frac{1}{4}-\frac{1}{4})+5\\
&=4[(x-\frac{1}{2})^2-\frac{1}{4}]+5\\
&=4(x-\frac{1}{2})^2+4
\end{align}


Llavors:

$$\int \frac{1}{4x^2-4x+5} dx=\frac{1}{4}\int \frac{1}{1+(x-\frac{1}{2})^2}=\frac{1}{4} tan^{-1}(x-\frac{1}{2})+C$$

###Integració per parts

La integració per parts la utilitzarem sempre que haguem d'integrar un producte de dues funcions diferents com per exemple:
- Polinomis i trigonomètriques
- Polinomis i exponencials
- Polinomis i logarítmiques
- Trigonomètriques i exponencials
- Trigonomètriques i logarítmiques
- etc.

Per mostrar la regla d'integració per parts, partirem de la regla de derivació del producte de dues funcions $f(x)\cdot g(x)$:

$$(f(x)g(x))^\prime=f^\prime(x)g(x)+f(x)g(x)^\prime$$

Si aïllem el terme $f(x)g^\prime(x)$ i prenem integrals a banda i banda obtenim:

$$\int f(x)g^\prime(x)=\int(f(x)g(x))^\prime-\int f^\prime(x)g(x) $$

per tant:

$$
\bbox[5px,border:2px solid black] { \int f(x)g^\prime(x)=f(x)g(x)-\int f^\prime(x)g(x)}
$$

Com a regla general, si tenim un polinomi multiplicat per una altra funció, al polinomi li assignarem sempre $f(x)$ i a la funció $g^\prime(x)$ perquè al integrar per segona vegada, al posar $f^\prime(x)$ farà baixar un grau al polinomi.

__Exemple 14__

$$\int x \sin(2x)dx=x\cdot (-\frac{1}{2} \cos (2x))-\int 1 (-\frac{1}{2}\cos (2x))dx= -\frac{x}{2} \cos (2x)+\frac{1}{4}\sin(2x)+C$$

__Exemple 15__

\begin{align}
\int x^2 \sin (3x) dx &= -\frac{1}{3}\int x^2 (-3 \sin(3x)) dx = -\frac{1}{3} \Big[x^2 \cos(3x)-\int 2x \cos (3x)dx \Big]=\\
&= -\frac{1}{3} \Big[x^2 \cos(3x)-\frac{1}{3}\int 2x (3 \cos (3x))dx \Big]=-\frac{1}{3} \Big[x^2 \cos(3x)-\frac{2}{3}\Big(x \sin (3x)-\int  \sin (3x)dx \Big)\Big]=\\
&=-\frac{1}{3} \Big[x^2 \cos(3x)-\frac{2}{3}(x \sin (3x)+\frac{1}{3} \cos (3x) \Big]+C=-\frac{x^3}{3} \cos(3x)+\frac{2}{9}x \sin (3x)-\frac{2}{27} \cos (3x)+C
\end{align}




###Mètode de substitució o de canvi de variables

Quan hem d'integrar funcions combinades que a simple vista resulten complicades, el mètode de canvi de variable és molt útil. A vegades resulta difícil, però amb la pràctica, s'acaba trobant el canvi adient. El canvi consistirà en substituir l'expressió de $x$ per una variable que li direm $t$, per exemple. De manera que:

$$t=f(x)\rightarrow dt=f^\prime(x)dx$$

D'altres vegades el que farem és substituir x per una expressió de $t$:

$$x=f(t)\rightarrow dx=f^\prime(t)dt$$

Ho veurem a través d'exemples perquè quedi més clar.

__Exemple 16__

$$\int \frac{dx}{x\sqrt{x^2-1}}$$

Per a calcular aquesta integral, aplicarem el canvi de variable que se'ns pot ocòrrer més immediat:

$$t=\sqrt{x^2-1}\rightarrow dt=\frac{1}{2\sqrt{x^2-1}}\cdot 2x dx =\frac{x}{\sqrt{x^2-1}}dx\rightarrow dx=\frac{dt\sqrt{x^2-1}}{x}=\frac{dt\cdot t}{x}$$

Si practiquem aquesta substitució a la integral de dalt obtenim:

$$\int \frac{dx}{x\sqrt{x^2-1}}=\int \frac{dt\cdot t}{x}\cdot \frac{1}{x\cdot t}=\int \frac{1}{1+t^2}dt=tan^{-1}(t)+C=tan^{-1}(\sqrt{x^2-1})+C$$

__Exemple 17__

Anem a veure un canvi de variable molt útil per integrals del tipus $\int \sqrt{a^2-x^2}dx$. Per a fer aquestes integrals emprarem el canvi: __$x= a \sin t$__ . Anem a calcular:

$$\int \sqrt{16-x^2} dx$$

Així doncs:

$$x=4\sin t \rightarrow dx=4 \cos t dt$$

Llavors:

$$\int \sqrt{16-x^2}dx=\int \sqrt{16-(4\sin t)^2}\cdot 4 \cos t dt=16\int \sqrt{\cos^2 t}\cos t dt= 16 \int \cos^2 t dt$$

Ara cal recordar les fòrmules trigonomètriques del cosinus de l'angle doble, $\cos 2t=\cos^2 t-\sin^2 t$ i que $\sin^2 t+\cos^2 t=1$. Llavors tenim:

$$\cos 2t=\cos^2 t-\sin^2 t= \cos^2 t- (1-\cos^2 t)=2 \cos^2 t-1\rightarrow \cos^2 t=\frac{\cos 2t+1}{2}$$

Fem aquesta substitució a la integral anterior i tenim:

$$\int \sqrt{16-x^2}dx=...=16\int \frac{\cos 2t+1}{2} dt=8 \int \cos 2t dt + 8 \int dt= 4\int 2 \cos 2t dt + 8 \int dt=4 \sin 2t + 8t+C$$

Ara ens cal desfer el canvi de variable. Abans de fer-ho apliquem la fòrmula del sinus de l'angle doble, $\sin 2t=2 \sin t \cos t$, a l'expressió anterior:

\begin{align}
\int \sqrt{16-x^2}dx=...&=4\cdot 2\sin t \cos t+8t+C=8 \sin t \sqrt(1-\sin^2 t)+8 t +C\\
&=8 \sin \big( \sin^{-1} \frac{x}{4}\big)\sqrt{1-\sin^2\big(sin^{-1}\frac{x}{4}\big)}+8 \sin^{-1}\frac{x}{4}+C\\
&=2x\sqrt{1-\big(\frac{x}{4}\big)^2}+8 \sin^{-1}\frac{x}{4}+C=2x\sqrt{\frac{16-x^2}{16}}+8 \sin^{-1}\frac{x}{4}+C\\
&=\frac{x}{2}\sqrt{16-x^2}+8 \sin^{-1}\frac{x}{4}+C
\end{align}

__Exemple 18__

Anem a veure un exemple d'integral de funció racional amb exponencials. En general, aquest tipus de funcions admeten el canvi $e^x=t$:

$$\int \frac{1+e^x}{1-e^x}dx$$

Amb aquest canvi:

$$t=e^x\rightarrow dt=e^x dx \rightarrow dx=\frac{dt}{e^x}=\frac{dt}{t}$$

Llavors tenim:

$$\int \frac{1+e^x}{1-e^x}dx = \int \frac{1+t}{1-t}\cdot \frac{dt}{t}=\int \frac{1+t}{t(1-t)}dt$$

Hem transformat la integral en una integral racional pròpia. Caldrà doncs fer la descomposició en fraccions parcials:

\begin{align}
\frac{1+t}{t(1-t)}&=\frac{A}{t}+\frac{B}{1-t}\\
1+t &=A(1-t)+B t\\
...\\
A&=1\\
B&=2\\
\end{align}

Tornem a la integral:

$$\int \frac{1+e^x}{1-e^x}dx =...=\int \frac{1}{t} dt+\int \frac{2}{1-t}dt=\ln t - 2 \ln (1-t)+C$$

Si desfem el canvi:

$$ \int \frac{1+e^x}{1-e^x}dx = \ln e^x -2 \ln (1-e^x)+C=\ln \Big(\frac{e^x}{(1-e^x)^2} \Big)+C$$

###Integrals trigonomètriques

Anomenem integrals trigonomètriques aquelles on en el seu integrand hi ha una combinació de funcions trigonomètriques. Algunes d'elles es poden resoldre per altres mètodes, però sovint, aplicant les diferents relacions entre raons trigonomètriques d'un angle, les podem transformar en integrals quasi-immediates. Això és el que veurem aquí.

####Integrals del tipus $\int \sin(x)^p \cdot \cos(x)^q dx$ on $p$ i $q$ són exponents parells.

Exemples d'integrals d'aquest tipus són: $\int \sin^2 x dx$, $\int \sin^4 x dx$, $\int \sin^2 x \cos^2 x dx$
Per a fer aquestes integrals, utilitzarem la fórmula trigonomètrica [del cosinus de l'angle doble](http://mdosil.cat/mates1batcientific/temes/trigonometria/#sinus-i-cosinus-de-langle-doble)  i també, el fet que la suma dels quadrats del sinus i cosinus d'un angle és sempre 1:

$$\cos 2x=\cos^2 x-sin^2 x$$

$$
\left.\begin{aligned}
 \cos 2x=\cos^2 x-sin^2 x\\
 \sin^2x+\cos^2x=1
\end{aligned}
\right\}
\rightarrow \cos^2x=\frac{\cos 2x+1}{2}\mbox{ ; } sin^2x=\frac{1-\cos 2x}{2}
$$


Anem a veure un parell d'exemples:

__Exemple 19__

$$\int \sin^2 x dx=\int \frac{1-\cos 2x}{2}dx=\int \frac{1}{2}dx -\frac{1}{2}\int 2 \cos 2x dx=\frac{1}{2}x-\frac{1}{4}\sin 2x +C$$


__Exemple 20__

\begin{align}
\int \sin^4 x dx&=\int (\sin^2 x)^2 dx=\int \Big(\frac{1-\cos2x}{2}\Big)^2 dx=\int \frac{1+\cos^2 2x - 2\cos 2x}{4}dx\\
&=\frac{1}{4}\int dx + \frac{1}{4} \int \cos^2 2x dx -\frac{1}{2}\int \cos 2x dx
\end{align}

Per resoldre la integral del mig, caldrà tornar a aplicar el mateix mètode i expressar el quadrat del cosinus en funció de l'angle doble:

$$\int \cos^2 2x dx=\int \frac{\cos 4x +1}{2} dx = \frac{1}{2}\frac{1}{4}\int 4 \cos 4x dx + \frac{1}{2} \int dx= \frac{1}{8}\sin 4x+\frac{1}{2}x +C$$

Per tant, la integral que volíem resoldre esdevé:

$$\int \sin^4 x dx=...=\frac{1}{4}x+\frac{1}{32}\sin 4x+\frac{1}{8} x -\frac{1}{4}\sin 2x+C=\frac{3}{8} x +\frac{1}{32}\sin 4x-\frac{1}{4}\sin 2x+C$$

####Integrals del tipus $\int \sin(x)^p \cdot \cos(x)^q dx$ on $p$ i $q$ són exponents almenys un d'ells senar.

D'aquestes integrals algunes poden ser quasi immediates, com per exemple:

$$\int \sin^4 x \cos x dx= \frac{\sin^5x}{5}+C$$

Per altres integrals, intentarem de transformar-les de tal manera que esdevinguin quasi immediates com la que acabem de veure. Anem a veure un exemple:

__Exemple 21__

\begin{align}
\int \sin^3 x \cos^5 x dx&= \int \cos x \sin^3 x \cos ^4 x dx=\int \cos x \sin^3 x (1-\sin^2 x)^2 dx\\
&=\int \cos x \sin^3 x (1+\sin^4 x-2\sin^2x)dx=\int \cos x \sin^3 x dx+\int \cos x \sin^7x dx - 2 \int \cos x \sin^5 x dx\\
&=\frac{\sin^4 x}{4}+\frac{\sin^8 x}{8}-\frac{\sin^6 x}{3}+C
\end{align}

####Integrals racionals amb $\sin x$ i $\cos x$

Aquestes integrals es solen fer per canvi de variable. El canvi de variable que funciona molt bé en aquests casos és:

$$t=\tan \frac{x}{2}$$

Per altra banda ens trobarem amb més freqüència integrals amb $\sin$ i $\cos$ que no pas amb $\tan$. El que podem fer és transformar aquest canvi per a cada cas utilitzant les identitats trigonomètriques. Per expressar el $\sin$ i $\cos$ en funció de $t$, utilitzarem les expressions següents:

\begin{align}
t=\tan \frac{x}{2}=\frac{\sin \frac{x}{2}}{\cos \frac{x}{2}}\\
\sin^2 \frac{x}{2}+\cos^2 \frac{x}{2}=1
\end{align}

El que volem ara és deduir, amb aquest canvi de variable, com es transformen $\sin x$ i $\cos x$. Partim de l'expressió següent per deduir-ho:

$$\sin^2 \frac{x}{2}+ \cos^2 \frac{x}{2}=1$$

Sabem també que: $\sin \frac{x}{2}=t \cos \frac{x}{2}$. Si substituïm això a l'expressió anterior obtenim:

$$\big(t \cos \frac{x}{2}\big)^2+\cos^2 \frac{x}{2}=1\rightarrow (t^2+1) \cos^2 \frac{x}{2}=1\rightarrow \cos^2 \frac{x}{2}=\frac{1}{t^2+1}$$

Guardem-nos aquest resultat i anem a veure com expressar $\sin \frac{x}{2}$ en funció de $t$. Sabem que:

$$\sin \frac{x}{2}=t \cos \frac{x}{2}$$

Si elevem al quadrat obtenim:

$$\sin^2 \frac{x}{2}=t^2 \cos^2\frac{x}{2}=\frac{t^2}{t^2+1}$$

També ens guardem aquest resultat. Ara tenim expressats el quadrat del cosinus i del sinus de l'angle meitat en funció de $t$. Aplicant les fòrmules del sinus i cosinus de [l'angle doble](http://mdosil.cat/mates1batcientific/temes/trigonometria/#sinus-i-cosinus-de-langle-doble) obtenim que:

$$\cos x= cos 2 \frac{x}{2}=\cos^2 \frac{x}{2}-\sin^2 \frac{x}{2}=\frac{1}{t^2+1}-\frac{t^2}{t^2+1}=\frac{1-t^2}{t^2+1}$$

Si fem el mateix per el sinus:

\begin{align}
\sin x&= \sin 2 \frac{x}{2}=2 \sin \frac{x}{2} \cos \frac{x}{2}=\frac{2 \sin \frac{x}{2}\cos \frac{x}{2}\cos \frac{x}{2}}{\cos \frac{x}{2}}\\
&=2 \tan \frac{x}{2}\cos^2 \frac{x}{2}=2t \frac{1}{t^2+1}=\frac{2t}{t^2+1}
\end{align}

Per tant, ja ho tenim. Ara només ens falta expressar el diferencial:

$$t=\tan \frac{x}{2} \rightarrow dt=(1+\tan^2 \frac{x}{2})\frac{1}{2}dx\rightarrow dx=\frac{2dt}{1+\tan^2 \frac{x}{2}}=\frac{2dt}{1+t^2}$$

Resumint:

\begin{align}
t&=\tan \frac{x}{2}\\
\sin x&=\frac{2t}{t^2+1}\\
\cos x&=\frac{1-t^2}{t^2+1}\\
dx&=\frac{2dt}{1+t^2}
\end{align}

__Exemple 22__

$$\int \frac{5}{1-\cos x}dx$$

Per a calcular-la farem el canvi anterior:

\begin{align}
\int \frac{5}{1-\cos x}dx&= \int \frac{5}{1-\frac{1-t^2}{1+t^2}}\frac{2dt}{1+t^2}=\int \frac{10 dt}{\frac{2t^2}{1+t^2}(1+t^2)}\\
&=5\int t^{-2}dt=-\frac{5}{t}+C=-\frac{5}{\tan \frac{x}{2}}+C
\end{align}

##Integrals definides
###Àrea sota la corba d'una funció

Considerem una funció contínua $f(x)$ en un interval tancat $[a,b]$. Ens interessa saber l'àrea sota la corba de la funció en aquest interval.
Una primera aproximació seria dividir l'interval $[a,b]$ en intervals iguals d'amplada $h$. Amb cadascun d'aquests intervals construïm un rectangle, un de superior i un de inferior, de tal manera que el superior sigui més gran que la corba i l'inferior, més petit.

Si sumem l'àrea dels rectangles superiors (suma de les bases per les altures de cadascun d'aquests rectangles) obtindríem una bona aproximació per excés de l'àrea sota la corba de la funció. Podríem fer el mateix sumant l'àrea dels rectangles inferiors, i n'obtindríem una aproximació per defecte. L'exemple següent ens dóna una idea de com serien aquests càlculs utilitzant la funció $f(x)=x^2+2$ entre dos punts concrets:

<iframe scrolling="no" title="integral definida" src="https://www.geogebra.org/material/iframe/id/TJscyCMT/width/717/height/585/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="717px" height="585px" style="border:0px;"> </iframe>

Si feu anar el lliscador per augmentar el nombre de rectangles, veureu que cada vegada la diferència entre l'àrea dels rectangles grans i l'àrea dels rectangles petits es fa més petita i s'aproxima més a l'àrea que hi ha sota la corba.

Així doncs, donada una funció contínua $f(x)$ en un interval tancat $[a,b]$, l'àrea definida sota la corba de la funció $f(x)$ entre els punts $a$ i $b$ es defineix com:

$$\int_{a}^{b} f(x)dx$$

de fet, aquesta integral és el límit de les sumes de les àrees de tots els rectangles quan l'amplada d'aquests ($h$) es fa molt petita. Si considerem que l'altura dels rectangles grans en cada interval és $M_i$ i la dels rectangles petits $m_i$ tenim que:

$$\mbox{ Àrea sota la corba}= \lim_{h\rightarrow 0} \sum_{x_i=a}^{x_i=b} h \cdot m_i=\lim_{h\rightarrow 0} \sum_{x_i=a}^{x_i=b} h \cdot M_i=\int_{a}^{b} f(x) dx$$

De fet, en matemàtiques, quan parlem d'una distància molt petita, l'anomenem _diferencial_. Per tant, $dx$ és una distància molt petita en l'eix de les abcisses. I quan aquests intervals es fan molt i molt petits, l'alçada del rectangle esdevé $f(x)$, d'aquí que $f(x)\cdot dx$ sigui l'àrea d'un rectangle molt petit de base $dx$ i alçada $f(x)$. I el símbol d'integral, en realitat és un sumatori de totes les àrees en l'interval.

La figura delimitada per l'eix de les abcisses, les dues rectes $x=a$ i $x=b$ i la corba de la funció $f(x)$ s'anomena __trapezi mixtilini__.

###Teorema fonamental del càlcul i regla de Barrow

El [Teorema fonamental del càlcul](https://es.khanacademy.org/math/integral-calculus/fundamental-theorem-of-calculus-ic) ens diu que donada una funció contínua $f(t)$ en un interval tancat $[a,b]$, si definim la funció àrea sota la corba de $f(x)$ com $F(x)=\int_{a}^{x} f(t) dt$, llavors, aquesta funció és una primitiva de $f(x)$:

$$\frac{dF}{dx}=\frac{d}{dx}\int_{a}^{x} f(t)dt=f(x)$$

<iframe scrolling="no" title="teorema fonamental del càlcul" src="https://www.geogebra.org/material/iframe/id/HtD8KNNp/width/500/height/632/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="500px" height="632px" style="border:0px;"> </iframe>

Això ens diu que qualsevol funció contínua $f(x)$ té una primitiva o antiderivada $F(x)$ i estableix una connexió entre derivades i integrals.

D'aquest teorema també se'n pot deduir la __Regla de Barrow__ que ens diu com podem calcular la integral definida entre 2 punts $a$ i $b$:

$$\bbox[5px,border:2px solid black] {\int_{a}^{b} f(x)dx= F(b)-F(a)}$$




###Propietats de la integral definida

Es pot demostrar que les integrals definides també compleixen les propietats següents:

1. $\int_{a}^{b} k \cdot f(x)dx= k\cdot \int_{a}^{b} f(x) dx$
2. $\int_{a}^{b} f(x)\pm g(x)dx= \int_{a}^{b} f(x) dx \pm \int_{a}^{b} g(x) dx$
3. Si $c \in [a,b]$ llavors: $\int_{a}^{b} f(x) dx=\int_{a}^{c} f(x) dx+\int_{c}^{b} f(x) dx$

###Àrea de recintes limitats per una funció entre dos punts i l'eix de les abcisses

D'aquesta manera podem calcular les àrees de regions delimitades per corbes evaluant només la primitiva de la funció entre els 2 punts els quals volem calcular l'àrea. Evidentment que l'àrea és una quantitat positiva. Per tant, per a calcular àrees caldrà tenir una sèrie de precaucions:

1. Donat un interval $[a,b]$, caldrà dividir la funció $f(x)$ en tants trossos com canvis de signe hi hagi a la funció.
2. En cadascun d'aquests intervals, l'àrea serà _el valor absolut_ de la integral definida entre els seus extrems.

Veiem-ho en un exemple concret.

__Exemple 23__

Calcula l'àrea del recinte limitat per la funció $f(x)=\sin x$ i l'eix de les abcisses entre els punts $0$ i $2\pi$.

<iframe scrolling="no" title="integral de sinx entre 0 i 2pi" src="https://www.geogebra.org/material/iframe/id/tB2ryvFM/width/500/height/300/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="500px" height="300px" style="border:0px;"> </iframe>

Per a calcular l'àrea haurem de dividir el gràfic entre dues regions: $R_1=[0,\pi]$ i $R_2=[\pi, 2\pi]$ ja que la funció s'anul.la en $x=\pi$. Anem a calcular cadascuna de les àrees.

\begin{align}
R_1=\int_{0}^{\pi} \sin x dx= [- \cos x]_{0}^{\pi}=-\cos \pi+\cos 0=2\\
R_2=|\int_{\pi}^{2\pi} \sin x dx|= |[- \cos x]_{\pi}^{2\pi}|=|-\cos 2\pi+\cos \pi|=2\\
\end{align}

Per tant:

$$A_{total}=R_1+R_2=4$$

###Àrea de recintes limitats per més d'una funció contínua

Quan hem de calcular l'àrea delimitada per dues o més funcions, aquest procés és una mica més llarg:


1. Primer ens caldrà buscar els punts de tall de les funcions. Si són dues, només ens cal igualar les seves expressions algebraiques i aïllar la $x$. Aquests punts ens defineixen els extrems de la integral definida.
2. Podem representar esquemàticament les funcions per saber, en l'interval definit pels punts de tall, quina és la funció més gran.
3. Calcularem l'àrea sota cada funció entre els 2 punts de tall, calculant la integral definida, en valor absolut.
4. Per trobar l'àrea resultant, en el cas de dues funcions, només ens cal restar les àrees sota les corbes, posant la corba més gran al davant.



__Exemple 24__

Calcula l'àrea compresa entre les funcions $f(x)=x^2$ i la funció $g(x)=x$.

Dibuixem aquestes gràfiques:

<iframe scrolling="no" title="Àrea delimitada per dues funcions" src="https://www.geogebra.org/material/iframe/id/fYFaWTyr/width/487/height/505/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="487px" height="505px" style="border:0px;"> </iframe>

Primer ens caldrà trobar els punts de tall de les dues funcions. Ens caldrà resoldre l'equació:

$$x^2=x \rightarrow x(x-1)=0\rightarrow x=0; x=1$$

Fixeu-vos que podem interpretar l'àrea com la resta de dues integrals definides:

$$A_{regió}=|\int_{0}^{1} x dx|-|\int_{0}^{1} x^2 dx|=|[\frac{x^2}{2}]_{0}^{1}|-|[\frac{x^3}{3}]_{0}^{1}|=\frac{1}{6}$$
