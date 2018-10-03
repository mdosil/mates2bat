#Tema 1: Derivades

##Derivada d'una funció en un punt

Aquest tema pretén definir el concepte de derivada a partir de la seva imatge geomètrica: el pendent de la recta tangent a una corba determinada en un punt concret. A partir d'aquí, definirem la funció derivada i introduirem la metodologia necessària per calcular de la derivada de qualsevol funció.

Per això, cal haver treballat prèviament els temes [*Funcions*](http://mdosil.cat/mates1batcientific/temes/funcions/) i [*Límits i continuïtat de funcions*](http://mdosil.cat/mates1batcientific/temes/limits/) de primer curs de batxillerat científico-tecnològic.


### Definició de derivada d'una funció en un punt



Donada una funció real $f$ i un punt d'abcissa $x=a$, $a \in \mathbb{R}$, on $a \in D_f$, considerem el límit següent:

$$\lim\limits_{h\to 0} \frac{f(a+h)-f(a)}{h}$$

si aquest límit existeix s'anomena **derivada de la funció $f$ en $x=a$, $f^{\prime} (a)$**:

$$\bbox[5px,border:2px solid black]{f^{\prime}(a)=\lim\limits_{h\to 0} \frac{f(a+h)-f(a)}{h}}$$

<iframe scrolling="no" title="interpretació geometric derivada (1)" src="https://www.geogebra.org/material/iframe/id/rcP7SKNk/width/639/height/393/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/true/ld/false/sdz/true/ctl/false" width="639px" height="393px" style="border:0px;"> </iframe>

Aquesta expressió es pot escriure d'una altra manera si adoptem el canvi de variable següent:

\begin{align}
a+h&=x \rightarrow \begin{cases} h=x-a \\
     \mbox{si } h \rightarrow 0 \Rightarrow x \rightarrow a
    \end{cases}
    \end{align}


$$\bbox[5px,border:2px solid black]{f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}}$$



**Exemple 1**

Donada $f(x)=7x-3$ calculeu $f^{\prime}(a) \forall a \in \mathbb{R}$.

$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{7x-3-(7a-3)}{x-a}=\lim\limits_{x\to a} \frac{7(x-a)}{x-a}=7$$

**Exemple 2**

Esbrineu si existeix la derivada en els punts $x=0$, $x=2$ i $x=-2$ de la funció a trossos:

$$f(x)= \begin{cases} 2x+1 \mbox{ si } x \le 0 \\
     x-1 \mbox{ si } x > 0
    \end{cases}$$

Per calcular la derivada en aquests punts, el que haurem de fer és calcular els límits anteriors per $x\to 0$, $x\to 2$ i $x \to -2$.

$$f^{\prime}(0)=\lim\limits_{x\to 0} \frac{f(x)-f(0)}{x-0}=?\Rightarrow\begin{cases} \lim\limits_{x\to 0^{+}} \frac{f(x)-f(0)}{x-0}= \lim\limits_{x\to 0^{+}} \frac{x-1-1}{x}=\lim\limits_{x\to 0^{+}} \frac{x-2}{x}=\frac{-2}{0}=-\infty\\
     \lim\limits_{x\to 0^{-}} \frac{f(x)-f(0)}{x-0}=\lim\limits_{x\to 0^{-}} \frac{2x}{x}=2
    \end{cases}$$

Veiem que els límits laterals no coincideixen. Per tant, el límit no es pot calcular, o sigui que **$f^{\prime}(0)=\nexists$**

$$f^{\prime}(2)=\lim\limits_{x\to 2} \frac{f(x)-f(2)}{x-2}=\lim\limits_{x\to 2} \frac{x-1-1}{x-2}=\lim\limits_{x\to 2} \frac{x-2}{x-2}=1$$

$$f^{\prime}(-2)=\lim\limits_{x\to -2} \frac{f(x)-f(-2)}{x+2}=\lim\limits_{x\to -2} \frac{2x+4}{x+2}=\lim\limits_{x\to -2} \frac{2(x+2)}{x+2}=2$$





###Interpretació geomètrica de la derivada

Anem a veure si amb un altre dibuix entenem què és això de la derivada. Fixeu-vos amb el gràfic següent:

<iframe scrolling="no" src="https://www.geogebra.org/material/iframe/id/bd7R3xbq/width/814/height/700/border/888888/rc/false/ai/false/sdz/true/smb/false/stb/false/stbh/true/ld/false/sri/true/at/auto" width="814px" height="700px" style="border:0px;"> </iframe>

Fixem-nos amb el gràfic de la funció f. Considerem dos punts, un punt $A$ de coordenades $(a, f(a))$ i un altre punt $B$ de coordenades $(x, f(x))$. Amb el punt lliscant podeu anar movent el punt $B$. Tracem una secant des del punt $A$ al punt $B$. Considerem el triangle dibuixat a la figura. El catet inferior té longitud $\Delta x=x-a$ i el catet superior $\Delta y=f(x)-f(a)$. El **pendent de la recta secant** és el quocient entre aquests dos valors i també coincideix amb **la tangent de l'angle $\alpha$**:

$$m=tan \alpha= \frac{\Delta y}{\Delta x}=\frac{f(x)-f(a)}{x-a}$$

D'altra banda, segurament a cursos anteriors vèieu que aquesta expressió també s'anomena **taxa de variació mitjana (TVM) entre $x$ i $a$**.

Si ens fixem aquesta fórmula és molt semblant a la de la definició de la derivada d'una funció en el punt $a$, $f^{\prime}(a)$. La diferència està en el **límit**.

Si ara anem acostant cada vegada més el punt $B$ al punt $A$, veiem que aquesta recta secant, en **el límit** que $A=B$ es converteix en una **recta tangent en $x=a$**, i per tant:

>La derivada en $x=a$ de $f(x)$, $f^\prime(a)$, és **el pendent de la recta tangent a la gràfica de la funció en el punt $x=a$**  i es calcula a partir del límit: $f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}$  

Per tant, també podem assegurar que si en $x=a$ la funció és **creixent(pendent positiu) $\Rightarrow f^{\prime}(a)>0$**, i al revés, si en $x=a$ la funció és **decreixent (pendent negatiu)$\Rightarrow f^{\prime}(a)<0$**.

###Definició de recta tangent a una corba en un punt

Vist això, anomenem recta tangent a una corba en el punt $x=a$, a aquella recta que compleix:

1. Conté el punt $(a,f(a))$
2. Té per pendent $m=f^{\prime}(a)$

D'aquí podem expressar l'equació de la recta tangent a una funció en el punt $x=a$ de la manera:




$$\bbox[5px,border:2px solid black]{y-f(a)=f^{\prime}(a)(x-a)}$$

**Exemple 3**

Trobeu l'equació de la recta tangent a la funció $f(x)=3x^2-5x+2$ en el punt d'abcissa $x=1$.

El punt $A$ en aquest cas és el punt $(1,f(1))=(1,0)$

Anem a calcular la derivada de la funció $f$ en $x=1$:



$$m=f^{\prime}(1)=\lim\limits_{x\to 1} \frac{f(x)-f(1)}{x-1}=\frac{3x^2-5x+2-0}{x-1}=1$$

Per tant, l'equació de la recta tangent a $f(x)$ en $x=1$ és:

$$y-0=1(x-1)\Rightarrow y=x-1$$


###Relació entre la derivada i la continuïtat d'una funció en un punt

Anem a demostrar el **teorema** següent:

> Si una funció $f$ és **derivable** en $x=a$ $\Rightarrow$ $f$ és **contínua** en aquest punt $x=a$

Cal notar que el recíproc de l'afirmació anterior no és cert: una funció pot ser contínua i no derivable en un punt. Però el que sí que es compleix és el contrari del teorema enunciat:

> Si una funció $f$ és **no és contínua** en $x=a$ $\Rightarrow$ $f$ **no és derivable** en aquest punt $x=a$

**Demostració**

Que una funció sigui derivable en el punt $x=a$ vol dir que està definida la seva derivada i en particular existeix el límit:

$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}$$

Si existeix el límit del quocient anterior, podem fer:



$$\lim\limits_{x\to a} \big(f(x)-f(a)\big)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}\cdot (x-a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}\cdot \lim\limits_{x\to a}(x-a)=f^{\prime}(a)\cdot 0=0$$

Per tant es compleix que:

$$ \lim\limits_{x\to a} \big(f(x)-f(a)\big)=0 \Rightarrow \lim\limits_{x\to a} f(x)-\lim\limits_{x\to a}f(a)=0 \Rightarrow \lim\limits_{x\to a} f(x)=\lim\limits_{x\to a}f(a)=f(a)$$

I arribem a la definició de funció contínua en un punt $x=a$: existeix el límit de la funció quan $x$ s'acosta a $a$ i aquest límit és igual a la imatge de $a$, $f(a)$:

$$\lim\limits_{x\to a} f(x)=f(a)$$

**Exemple 4**

Digues si la funció a trossos

$$f(x)= \begin{cases} 2x^2-3x-1 \mbox{ si } x \le -1 \\
     4x+1 \mbox{ si } -1 < x < 2 \\
     9 \mbox{ si } x \ge 2
    \end{cases}$$


és:

1. Derivable en $x=-1$, $x=0$ i $x=2$
2. És contínua en aquests punts

Anem a veure si és derivable en aquests punts. Calcularem la derivada a partir del límit i en els casos que la funció estigui definida de manera diferent per la dreta i per l'esquerra dels punts calcularem els límits laterals.

$$f^{\prime}(-1)= \lim\limits_{x\to -1} \frac{f(x)-f(-1)}{x+1} \begin{cases} \lim\limits_{x\to -1^+} \frac{4x+1-4}{x+1}= \lim\limits_{x\to -1^+} \frac{4x-3}{x+1}=-\infty\\
     \lim\limits_{x\to -1^-} \frac{(2x^2-3x-1)-(2(-1)^2-3(-1)-1)}{x+1}= \lim\limits_{x\to -1^-} \frac{2x^2-3x-5}{x+1}=\lim\limits_{x\to -1^-} \frac{(2x-5)(x+1)}{x+1}=-7
    \end{cases}$$

$f(x)$ no és derivable en $x=-1$.

$$f^{\prime}(0)= \lim\limits_{x\to 0} \frac{f(x)-f(0)}{x-0}= \lim\limits_{x\to 0} \frac{4x+1-1}{x}=4$$

**$f(x)$ és derivable en $x=0$** i $f^{\prime}(0)=4$.


$$f^{\prime}(2)= \lim\limits_{x\to 2} \frac{f(x)-f(2)}{x-2} \begin{cases} \lim\limits_{x\to 2^+} \frac{9-9}{x-2}=0\\
    \lim\limits_{x\to 2^-} \frac{4x+1-9}{x-2}= \lim\limits_{x\to 2^-} \frac{4(x-2)}{x-2}=4
    \end{cases}$$

$f(x)$ no és derivable en $x=2$ ja que els límits laterals no coincideixen.

En els casos que la funció és derivable la funció serà contínua en aquests punts. Per tant, **en $x=0$ la funció és contínua i derivable**. Però pot ser que no sigui derivable i en canvi, sí que sigui contínua. Anem a veure què passa en $x=-1$ i $x=2$:

$$\lim\limits_{x\to -1} f(x)=\begin{cases} \lim\limits_{x\to -1^+} (4x+1)= -3\\
     \lim\limits_{x\to -1^-} (2x^2-3x-1)= 4
    \end{cases}$$

Com que els límits laterals no coincideixen **$f(x)$ no és derivable ni contínua en $x=-1$**


$$\lim\limits_{x\to 2} f(x)=\begin{cases} \lim\limits_{x\to 2^+} 9= 9\\
     \lim\limits_{x\to 2^-} (4x+1)= 9
    \end{cases}$$

Com que els límits laterals sí que coincideixen **$f(x)$ no és derivable però sí contínua en $x=-1$**

Si mireu la representació gràfica de la funció i què passa en aquests punts en concret, entendreu més coses.

<iframe scrolling="no" src="https://www.geogebra.org/material/iframe/id/FU6xp4g7/width/700/height/500/border/888888/rc/false/ai/false/sdz/true/smb/false/stb/false/stbh/true/ld/false/sri/true/at/auto" width="700px" height="500px" style="border:0px;"> </iframe>

##La funció derivada

###Definició de funció derivada

Sigui $f$ una funció real de domini $A$ i **contínua** en tot $a \in A$. Anomenem **funció derivada de $f$** (o derivada de $f$) a aquella funció que representem per $f^\prime$ de domini $A$ que associa a tot element d'$A$ la derivada d'aquesta funció en aquest punt:

\begin{align}
f^\prime : A & \rightarrow \mathbb{R} \\
x & \rightarrow y=f^\prime (x)= \lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}
\end{align}

**Exemple 5**

Calcula la funció derivada de la funció $f(x)=x^2+1$.


$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{x^2+1-a^2-1}{x-a}=lim_{x\to a} \frac{(x+a)(x-a)}{x-a}=a+a=2a \forall a \in \mathbb{R}$$

Per tant: $f^\prime (x)=2x$ és la derivada de $f(x)=x^2+1$.


##Regles de derivació

Aplicant la definició de derivada (càlcul del límit), podem llistar les derivades de les funcions més comunes. Demostrarem les 4 primeres regles de derivació i la resta les posarem en una taula. En aquest [enllaç](https://www.khanacademy.org/math/ap-calculus-bc/bc-derivative-rules) trobareu més informació de les regles de derivació així com els vídeos amb la seva demostració.


**Regla 1**

>Si $f(x)=k$, $k\in \mathbb{R} \Rightarrow f^\prime(x)=0$

*Demostració*

$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{c-c}{x-a}=\lim\limits_{x\to a} \frac{0}{x-a}=\lim\limits_{x\to a} 0= 0$$

**Regla 2**

>Si $f(x)=x \Rightarrow f^\prime(x)=1$

*Demostració*

$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{x-a}{x-a}=\lim\limits_{x\to a} 1=1$$

**Regla 3**

>Si $f$ i $g$ són funcions derivables $\Rightarrow f+g$ també és derivable i es compleix: $(f+g)^\prime (x)=f^\prime(x)+g^\prime(x)$.

*Demostració*

$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{(f+g)(x)-(f+g)(a)}{x-a}=\lim\limits_{x\to a} \frac{f(x)+g(x)-f(a)-g(a)}{x-a}=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{g(x)-g(a)}{x-a}=f^\prime(a)+g^\prime(a) \forall a$$


**Regla 4**

>Si $f$ és una funció derivable $\Rightarrow K\cdot f$ on $K \in \mathbb{R}$ també és derivable i es compleix: $(K\cdot f)^\prime (x)=K \cdot f^\prime(x)$.

*Demostració*

$$f^{\prime}(a)=\lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=\lim\limits_{x\to a} \frac{(K\cdot f)(x)-(K \cdot f)(a)}{x-a}=\lim\limits_{x\to a} \frac{K\cdot (f(x)-f(a)}{x-a}=\lim\limits_{x\to a} K \cdot  \lim\limits_{x\to a} \frac{f(x)-f(a)}{x-a}=K \cdot f^\prime (a)$$

###Taula de derivades

| Funció     | Derivada |
| :------------- |:------------- |
| Constant      |$$(k)^{\prime}=0 \forall k \in \mathbb{R}$$|
| Identitat      |$$x^{\prime}=1 $$|
| Suma      |$$(f(x)+g(x))^{\prime}=f^{\prime}(x)+g^{\prime}(x)$$|
| Producte per un nombre      |$$(k\cdot f(x))^{\prime}=k \cdot f^{\prime}(x)$$|
| Potència      |$$(x^n)^{\prime}=n\cdot x^{n-1}$$|
|Polinomi:  |$[a_n x^n+a_{n-1}x^{n-1}+...+a_2 x^2+a_1 x+a_0]^\prime=n\cdot a_n x^{n-1}+(n-1)\cdot a_{n-1}x^{n-2}+...+2\cdot a_2 x+a_1$|
| Producte      |$$(f(x)\cdot g(x))^{\prime}=f^{\prime}(x)\cdot g(x)+f(x)\cdot g^{\prime} (x)$$|
| Quocient      |$$\Big(\frac{f(x)}{g(x)}\Big)^{\prime}=\frac{f^{\prime}(x)\cdot g(x)-f(x)\cdot g^{\prime}(x)}{g(x)^2}$$|
| Trigonomètriques      |$$\big(\sin(x)\big)^{\prime}=\cos(x)$$|
|       |$$\big(\cos(x)\big)^{\prime}=-\sin(x)$$|
|      |$$\big(\tan(x)\big)^{\prime}=1+\tan^2(x)$$|
| Inverses Trigonomètriques      |$$\big(arcsin(x)\big)^{\prime}=\frac{1}{\sqrt{1-x^2}}$$|
|       |$$\big(arccos(x)\big)^{\prime}=-\frac{1}{\sqrt{1-x^2}}$$|
|      |$$\big(arctan(x)\big)^{\prime}=\frac{1}{1+x^2}$$|
| Composició (regla de la cadena)|$$\big(f(g(x))\big)^{\prime}=f^{\prime}\big(g(x)\big)\cdot g^{\prime}(x)$$|
|Exponencials|$$\big(e^x\big)^{\prime}=e^x$$|
||$$\big(a^x\big)^{\prime}=a^x\cdot ln(a)$$|
|Logarítmiques| $$\big(ln(x)\big)^{\prime}=\frac{1}{x}$$|
||$$\big(log_a(x)\big)^{\prime}=\frac{1}{x}\cdot \frac{1}{ln(a)}$$|

###Exemples

**Exemple 6: Derivada d'un quocient**

Troba la derivada de la funció següent: $f(x)=\frac{x^2}{sin(x)}$.

Com que és un quocient:

\begin{align}
f(x)^{^{\prime}}&=\frac{(x^2)^{\prime}\cdot sin(x)-x^2\cdot \big(sin(x)\big)^{\prime}}{sin^2(x)} \\
&=\frac{2x\cdot sin(x)-x^2\cdot cos(x)}{sin^2(x)}=\frac{2x-x^2\cdot tan(x)}{sin(x)}
\end{align}

**Exemple 7: Derivada d'una funció composta**

Troba la derivada de la funció següent: $f(x)=sin(ln(x+1))$.

Veiem que aquest és el resultat de la composició de dues funcions, la funció $sin(x)$ i la funció $ln(x+1)$. Per tant, primer apliquem la regla de derivació de la funció sinus i llavors derivem la segona funció:

$$f(x)^{\prime}=cos \big( ln(x+1)\big)\cdot \Big(ln(x+1)\Big)^{\prime}=cos \big( ln(x+1)\big)\cdot \frac{1}{x+1}$$


**Exemple 8: Derivació logarítmica**

Troba la derivada de la funció següent: $f(x)=x^{sin(x)}$.

A vegades cal aplicar *trucs* per poder derivar algunes funcions. Quan tenim funcions a l'exponent, el més pràctic és treure el logaritme a banda i banda de l'expressió donada i derivar després:

\begin{align}
f(x)&=x^{sin(x)}\\
ln\big(f(x)\big)&=sin(x)\cdot ln(x)\\
\frac{1}{f(x)} \cdot f(x)^{\prime}&=cos(x)\cdot ln(x)+sin x \cdot \frac{1}{x}\\
f(x)^{\prime}&=f(x)\cdot \Big(cos(x)\cdot ln(x)+\frac{1}{x}\cdot sin(x)\Big)\\
f(x)^{\prime}&=x^{sin(x)} \Big(cos(x)\cdot ln(x)+\frac{1}{x}\cdot sin(x)\Big)\\
\end{align}

##Derivació successiva

El procés de càlcul de la derivada es pot dur a terme moltes vegades. De fet, si prenem la definició de la derivada com a límit, tenim que:



\begin{align}
f(x)^{\prime} &= \lim\limits_{h\to 0} \frac{f(x+h)-f(x)}{h}\\
f(x)^{\prime \prime} &= \lim\limits_{h\to 0} \frac{f(x+h)^{\prime} -f(x)^{\prime} }{h}\\
f(x)^{\prime \prime \prime} &= \lim\limits_{h\to 0} \frac{f(x+h)^{\prime \prime} -f(x) ^{\prime \prime}}{h}\\
.\\
.\\
.\\
f(x)^{n} &= \lim\limits_{h\to 0} \frac{f(x+h)^{n-1}-f(x)^{n-1}}{h}\\
\end{align}

on $f(x)^{n}$ és la derivada $n$-èssima de $f(x)$.


**Exemple 9: Calcula la derivada d'ordre n de la funció: f(x)=ln(x+1)**

\begin{align}
f(x)^{\prime} &= \frac{1}{x+1}\\
f(x)^{\prime \prime} &= \frac{-1}{(x+1)^2}\\
f(x)^{\prime \prime \prime} &= \frac{2(x+1)}{(x+1)^4}=\frac{2}{(x+1)^3}\\
f(x)^4&= \frac{-2\cdot 3 (x+1)^2}{(x+1)^6}=\frac{-6}{(x+1)^4}\\
.\\
.\\
.\\
f(x)^{n} &=\frac{(-1)^{n+1}(n-1)!}{(x+1)^n}\\
\end{align}
