#Tema 2: Funcions contínues i derivables


##Introducció

###Funció contínua

En el [curs anterior](http://mdosil.cat/mates1batcientific/temes/limits/) vam veure que una *funció era contínua en un punt $x=a$* si existia el seu límit i coincidia amb la seva imatge:

$f(x)$ és contínua en $x=a \Leftrightarrow \lim_{x\to a^{-}}f(x)=\lim_{x\to a^{+}}f(x)=f(a)$

Així doncs, una funció serà *contínua en un interval tancat $[a,b]$* si:

* És contínua $\forall x \in (a,b)$
* $\lim_{x\to a^{+} }f(x)=f(a)$
* $\lim_{x\to b^{-} }f(x)=f(b)$

###Funció derivable

Del [tema anterior](http://mdosil.cat/mates2batcientific/temes/derivades/) se'n dedueix que una *funció és derivable en un punt $x=a$* si existeixen les derivades laterals $f^\prime (a)^{-}$ i $f^\prime (a)^{+}$ i coincideixen:

$$f^\prime (a)^{-}= f^\prime (a)^{+}$$

on:

\begin{align}
f^\prime (a)^{-}=\lim_{x\to a^{-} } \frac{f(x)-f(a)}{x-a}\\
f^\prime (a)^{+}=\lim_{x\to a^{+} } \frac{f(x)-f(a)}{x-a}
\end{align}

De la mateixa manera, una funció és *derivable en un interval tancat $[a,b]$* si:

* És derivable $\forall x \in (a,b)$
* Existeixen $f^\prime (a)^{+}$ i $f^\prime (b)^{-}$

##Teoremes sobre funcions contínues


###Teorema de Bolzano

Sigui $f(x)$ una funció __contínua__ en un interval tancat $[a,b]$. Si $f(a)$ i $f(b)$ tenen signes oposats ($f(a)\cdot f(b)<0$) podem assegurar que existeix un punt $c$ de l'interval $[a,b]$ on $f(c)=0$ (la funció talla l'eix de les $x$):

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua en } [a,b] \\
f(a) \cdot f(b)<0
\end{aligned}
\right\}
\rightarrow \exists c \in (a,b) | f(c)=0 }
$$

<iframe scrolling="no" title="Teorema de Bolzano" src="https://www.geogebra.org/material/iframe/id/syyBEjue/width/400/height/500/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="400px" height="500px" style="border:0px;"> </iframe>

La condició de *continuïtat* en l'interval **és totalment necessària**. Si la funció no és contínua, el teorema no té perquè ser cert.

Aquest teorema ens és útil per a trobar arrels (zeros) d'una funció en un determinat interval.

Cal també notar que el Teorema de Bolzano ens diu que com a mínim la funció talla en un punt, però n'hi poden haver més, de punts de tall.

__Exemple 1__

Prova que l'equació $x^3-3x+1=0$ té una arrel en l'interval $[1,2]$. Calculeu-la amb un error més petit que una dècima.

Veiem que: $f(1)=-1$ i $f(2)=3$. Per tant, ha d'existir un punt $c \in [1,2]$ on es compleixi que $f(c)=0$. Utilitzarem el mètode de tempteig per a trobar una aproximació a aquest punt:


\begin{align}
f(1.5)&<0 \rightarrow c \in [1.5,2]\\
f(1.7)&>0 \rightarrow c \in [1.5,1.7]\\
f(1.6)&>0 \rightarrow c \in [1.5,1.6]\\
f(1.55)&>0 \rightarrow c \in [1.5,1.55]\\
f(1.52)&<0 \rightarrow c \in [1.52,1.55]\\
f(1.53)&<0 \rightarrow c \in [1.53,1.55]\\
f(1.54)&>0 \rightarrow c \in [1.53,1.54]\\
\end{align}

Per tant, el valor $c$ que estem buscant és $c=1.53...$, el $3$ és xifra significativa, per tant, ja l'hem trobat amb un error més petit que una dècima.

__Exemple 2__

Demostreu que hi ha un número real $x$ tal que el seu cosinus és igual a la mateixa $x$. Doneu una aproximació d'aquest valor.

D'entrada l'enunciat d'aquest problema ens sembla molt extrany. Anem a interpretar-lo. Hem de resoldre:


$$\cos(x)=x$$

Considerem ara la funció $f(x)=\cos(x)-x$. Si trobem dos punts d'aquesta funció que tinguin signes oposats, com que $f(x)$ és contínua, podem garantir, pel teorema de Bolzano que la funció tindrà un arrel (zero) dins d'aquest interval, i per tant es complirà:

$f(x)=\cos(x)-x=0$.

Veiem que:


\begin{align}
f(0)&=\cos(0)-0=1 >0\\
f\Big(\frac{\pi}{2}\Big)&=\cos\Big(\frac{\pi}{2}\Big)-\frac{\pi}{2}=-\frac{\pi}{2} <0\\
\end{align}

Per tant, podem afirmar que existeix un punt $a$ dins l'interval $(0,\frac{\pi}{2})$ tal que $f(a)=0$, o sigui que el seu cosinus és igual a ell mateix:

$$\cos(a)-a=0 \rightarrow \cos(a)=a$$

Per trobar aquest valor, haurem d'aplicar el mètode de tempteig:


\begin{align}
f\Big(\frac{\pi}{4}\Big)&<0 \rightarrow a \in \Big[0,\frac{\pi}{4}\Big]\\
f\Big(\frac{\pi}{8}\Big)&>0 \rightarrow a \in \Big[\frac{\pi}{8},\frac{\pi}{4}\Big]\\
f\Big(\frac{\pi}{5}\Big)&>0 \rightarrow a \in \Big[\frac{\pi}{5},\frac{\pi}{4}\Big]\\
&.\\
&.\\
&.\\
&.
\end{align}

El valor que estem buscant està entre $\Big[\frac{\pi}{5},\frac{\pi}{4}\Big]$



###Teorema dels Valors intermitjos

El Teorema dels Valors intermitjos és una generalització del Teorema de Bolzano:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua en } [a,b] \\
f(a) < c < f(b)
\end{aligned}
\right\}
\rightarrow \exists x \in (a,b) | f(x)=c }
$$

Dit d'una altra manera: *la funció pren tots els valors intermitjos entre $f(a)$ i $f(b)$*.

<iframe scrolling="no" title="Teorema dels valors intermitjos" src="https://www.geogebra.org/material/iframe/id/vUcujT6h/width/412/height/652/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="412px" height="652px" style="border:0px;"> </iframe>

Igual que en el Teorema de Bolzano, si la funció no és contínua en l'interval, el teorema no té perquè ser cert.

###Teorema de Weierstrass

Si $f(x)$ és una funció contínua en un interval *compacte* (tancat i acotat) $[a,b]$, podem assegurar que sempre hi haurà com a mínim un **màxim absolut** i un **mínim absolut** de la funció $f(x)$ dins l'interval $[a,b]$. Això és:


$$
\bbox[5px,border:2px solid black] {
f(x) \mbox{ contínua en } [a,b] \rightarrow \exists x_1, x_2 \in [a,b] | f(x_1) \le f(x) \le f(x_2) }
$$

la funció $f(x)$ transcorre entre els valors de $f(x_1)$ i $f(x_2)$.

<iframe scrolling="no" title="Teorema de Weierstrass" src="https://www.geogebra.org/material/iframe/id/ZsuUzP38/width/774/height/394/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="774px" height="394px" style="border:0px;"> </iframe>

En el cas del gràfic, $x_1$ és mínim absolut i $x_2$ màxim absolut.

##Teoremes sobre funcions derivables

Anem a veure alguns teoremes que compleixen les funcions derivables.

###Teorema de Rolle

Sigui $f(x)$ una funció __contínua__ en un interval tancat $[a,b]$ i __derivable__ en $(a,b)$. Si $f(a)= f(b)$ podem assegurar que existeix un punt $c$ de l'interval $(a,b)$ on $f^\prime(c)=0$:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua en } [a,b] \\
f(x) \mbox{ derivable en } (a,b) \\
f(a)=f(b)
\end{aligned}
\right\}
\rightarrow \exists c \in (a,b) | f^\prime(c)=0 }
$$

Podeu trobar-ne la demostració a la [wikipèdia](https://es.wikipedia.org/wiki/Teorema_de_Rolle).

<iframe scrolling="no" title="Teorema de Rolle" src="https://www.geogebra.org/material/iframe/id/uD8Tkr8s/width/517/height/654/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="517px" height="654px" style="border:0px;"> </iframe>


###Teorema del Valor mig (de Lagrange)

Sigui una funció contínua $f(x)$ en un interval tancat $[a,b]$ i derivable en $(a,b)$. Llavors podem afirmar que existeix un punt $c$ de l'interval $(a,b)$ que la seva derivada (o el que és el mateix, el pendent de la recta tangent a $x=c$) és igual al pendent de la recta *secant* que uneix els punts $(a, f(a))$ i $(b, f(b))$:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua en } [a,b] \\
f(x) \mbox{ derivable en } (a,b)
\end{aligned}
\right\}
\rightarrow \exists c \in (a,b) | f^\prime(c)= \frac{f(b)-f(a)}{b-a}}
$$

on $m_{ab}=\frac{f(b)-f(a)}{b-a}$ és el pendent de la recta secant que uneix els punts $(a, f(a))$ i $(b, f(b))$. La demostració d'aquest teorema es pot trobar a la [wikipèdia](https://es.wikipedia.org/wiki/Teorema_del_valor_medio).

Fixem-nos que el Teorema de Rolle enunciat abans és un cas particular del Teorema del Valor mig: si $f(a)=f(b)$, la recta secant que uneix els punts $(a, f(a))$ i $(b, f(b))$ és *horitzonal* i en conseqüència, té pendent $0$. Per tant, el punt $c$ en aquest cas, tindrà derivada $0$.

<iframe scrolling="no" title="Teorema del Valor mig (de Lagrange)" src="https://www.geogebra.org/material/iframe/id/ZmEMysaT/width/556/height/525/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="556px" height="525px" style="border:0px;"> </iframe>



###Teorema de Cauchy

Siguin $f(x)$ i $g(x)$ funcions contínues en un interval tancat $[a,b]$ i derivables en $(a,b)$. Llavors podem afirmar que existeix un punt $c$ de l'interval $(a,b)$ on es compleix: $\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f^\prime(c)}{g^\prime(c)}$.

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ i } g(x) \mbox{ contínues en } [a,b] \\
f(x)  \mbox{ i } g(x)\mbox{ derivables en } (a,b)
\end{aligned}
\right\}
\rightarrow \exists c \in (a,b) | \frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f^\prime(c)}{g^\prime(c)}}
$$

La demostració del Teorema de Cauchy es pot trobar a la [wikipèdia](https://es.wikipedia.org/wiki/Teorema_del_valor_medio_de_Cauchy).

Notem que el Teorema del Valor mig (de Lagrange) és un cas particular del Teorema de Cauchy en que $g(x)=x$:


$$
\left.\begin{aligned}
g(b)=b \\
g(a)=a \\
g^\prime(x)=1
\end{aligned}
\right\}
\rightarrow \frac{f(b)-f(a)}{b-a}=f^\prime(c)
$$



##Aplicacions de la derivada a l'estudi d'una funció

Els teoremes anteriorment anunciats ens permeten aplicar-los a l'estudi d'una funció. Ens fixarem aquí en 3 de les característiques de les funcions, el creixement i decreixement, els extrems locals i els punts d'inflexió.

###Creixement i decreixement

En apartats anteriors vèiem que la derivada en un punt és el pendent de la recta tangent a la funció en aquest punt. Per tant, si la funció és creixent en aquest punt, el pendent de la recta tangent serà positiu (i per tant la derivada també). D'altra banda, si la funció és decreixent en aquest punt, el pendent de la recta tangent serà negatiu així com la seva derivada:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua i derivable en } x=a \\
f^\prime(a) > 0
\end{aligned}
\right\}
\rightarrow f(x) \mbox{ és creixent en } x=a}
$$
$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua i derivable en } x=a \\
f^\prime(a) < 0
\end{aligned}
\right\}
\rightarrow f(x) \mbox{ és decreixent en } x=a}
$$

Les implicacions al revés no són certes: per exemple, si una funció és derivable en $x=a$ i és creixent en aquest punt, no podem afirmar que la derivada sigui positiva en aquest punt. Com veurem més endavant, aquesta derivada pot ser també $0$. Per exemple, la funció $f(x)=x^3$ té derivada zero en $x=0$ i en canvi és creixent en aquest punt:

<iframe scrolling="no" title="Creixement i decreixement d'una funció" src="https://www.geogebra.org/material/iframe/id/fdrEZM84/width/528/height/399/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="528px" height="399px" style="border:0px;"> </iframe>

###Màxims i mínims locals

Per tal que hi hagi un màxim o un mínim d'una funció derivable $f(x)$ en un punt $x=a$ necessàriament la derivada de la funció en aquest punt ha de ser zero: $f^\prime(a)=0$, perquè en cas contrari, la funció seria creixent o decreixent en aquest punt, com acabem de veure:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ té un extrem local } x=a \\
f(x) \mbox{ és derivable en } x=a
\end{aligned}
\right\}
\rightarrow f^\prime(a)=0}
$$

La condició que la derivada valgui $0$ és una *condició necessària* per tal que en el punt $x=a$ hi pugui haver un extrem local (màxim o mínim).Aquests punts s'anomenen **punts singulars** o **punts estacionaris**.

Tot i això, aquesta no és una *condició suficient*. Això vol dir que el fet que la derivada valgui zero en un punt no ens diu que en aquell punt hi hagi un extrem local. La funció $f(x)=x^3$ té derivada $0$ en $x=0$ i en canvi no té un màxim ni un mínim en aquest punt:

<iframe scrolling="no" title="ics al cub no extrem local" src="https://www.geogebra.org/material/iframe/id/tTtNVqkG/width/525/height/514/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="525px" height="514px" style="border:0px;"> </iframe>

Per saber si un extrem local és màxim o mínim haurem de fer un estudi del signe de la segona derivada. Es pot demostrar que:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua i derivable en } x=a \\
f^\prime(a) = 0 \\
f^{\prime \prime}(a) < 0
\end{aligned}
\right\}
\rightarrow f(x) \mbox{ té un màxim local en } x=a}
$$

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua i derivable en } x=a \\
f^\prime(a) = 0 \\
f^{\prime \prime}(a) > 0
\end{aligned}
\right\}
\rightarrow f(x) \mbox{ té un mínim local en } x=a}
$$

En cas que la segona derivada fos també $0$, $f^{\prime \prime}(a)=0$, hauríem de continuar derivant. Si la tercera és no nul.la, no hi ha extrem local en $x=a$. Si és zero hauríem de buscar la quarta derivada. En cas que fos positiva, en $x=a$ hi hauria un mínim local, i si fos negativa un màxim local. Si la quarta fos també zero, hauríem de continuar el procés. Com a regla general:

\begin{align}
f^\prime (a)&=0 \rightarrow
\begin{cases} f^{\prime \prime} (a)>0 \rightarrow \mbox{ mínim local en } x=a \\
     f^{\prime \prime} (a)<0 \rightarrow \mbox{ màxim local en } x=a \\
     f^{\prime \prime} (a)=0 \rightarrow
     \begin{cases} f^{\prime \prime \prime} (a)\ne 0 \rightarrow \mbox{ no hi ha extrem local en } x=a \\
          f^{\prime \prime \prime} (a)=0 \rightarrow
          \begin{cases} f^{iv} (a) > 0 \rightarrow \mbox{ mínim local en } x=a \\
          f^{iv} (a) < 0 \rightarrow \mbox{ màxim local en } x=a \\
               f^{iv} (a)=0 \rightarrow
                 \begin{cases}
                 ...
                 \end{cases}
              \end{cases}
         \end{cases}
    \end{cases}
    \end{align}

Resumint: si $n$ és la primera derivada no nul.la en $x=a$: $f^{n}(a)\ne 0 $ llavors:

* Si $n$ és imparell **no hi ha extrem local**
* Si $n$ és parell:
\begin{align}
f^n(a)>0 \rightarrow \mbox{ mínim local en }x=a\\
f^n(a)<0 \rightarrow \mbox{ màxim local en }x=a
\end{align}

**Exemple 3**

Digues si la funció $f(x)=(x-1)^4$ té algun extrem local.

* Busquem la primera derivada i la igualem a zero:

$$f^\prime(x)=4(x-1)^3=0 \rightarrow  x=1 \mbox{ punt singular}$$

* Busquem la segona derivada i l'avaluem en $x=1$:

$$f^{\prime \prime}(x)=12(x-1)^2 \rightarrow  f^{\prime \prime}(1)=0 \mbox{ cal buscar la 3a derivada}$$

* Busquem la tercera derivada i l'avaluem en $x=1$:

$$f^{\prime \prime \prime}(x)=24(x-1) \rightarrow  f^{\prime \prime \prime}(1)=0 \mbox{ cal buscar la 4a derivada}$$


* Busquem la quarta derivada i l'avaluem en $x=1$:

$$f^{iv}(x)=24 \rightarrow  f^{iv}(1)=24 > 0 \mbox{ en } x=1 \mbox{ hi ha un mínim local }$$

Anem a representar la funció per a comprovar-ho:

<iframe scrolling="no" title="minim local" src="https://www.geogebra.org/material/iframe/id/AsATwqXC/width/434/height/609/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="434px" height="609px" style="border:0px;"> </iframe>

###Concavitat i convexitat

Per saber si una funció és cóncava o convexa en un punt, cal buscar el signe de la segona derivada:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua i dues vegades derivable en } x=a \\
f^{\prime \prime}(a) > 0
\end{aligned}
\right\}
\rightarrow f(x) \mbox{ és còncava en } x=a}
$$

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ contínua i dues vegades derivable en } x=a \\
f^{\prime \prime}(a) < 0
\end{aligned}
\right\}
\rightarrow f(x) \mbox{ és convexa en } x=a}
$$

Si ens fixem bé, en el cas de mínims locals, la funció és sempre còncava en el punt (segona derivada positiva) i en el cas de màxims, sempre és convexa (segona derivada negativa).

En l'exemple anterior, la segona derivada de la funció $f(x)=12(x-1)^2$ sempre és positiva (excepte en el punt $x=1$ que val zero). Per tant, podem afirmar que la funció serà còncava en tot el seu domini.

###Punts d'inflexió

Un punt d'inflexió és aquell punt on la funció passa de ser còncava a convexa o a l'inrevés. Es pot demostrar que:

$$
\bbox[5px,border:2px solid black] {\left.\begin{aligned}
f(x) \mbox{ té un punt d'inflexió } x=a \\
f(x) \mbox{ dues vegades derivable en } x=a
\end{aligned}
\right\}
\rightarrow f^{\prime \prime}(a)=0}
$$

Com a regla general:

\begin{align}
f^{\prime \prime} (a)&=0 \rightarrow
\begin{cases} f^{\prime \prime \prime} (a) \ne 0 \rightarrow \mbox{ punt d'inflexió en } x=a \\
     f^{\prime \prime \prime} (a)=0 \rightarrow
     \begin{cases} f^{iv} (a)\ne 0 \rightarrow \mbox{ no hi ha punt d'inflexió en } x=a \mbox{ (la funció o bé és còncava o convexa en aquest punt) }\\
          f^{iv} (a)=0 \rightarrow
          \begin{cases} f^{v} (a) \ne 0 \rightarrow \mbox{ punt d'inflexió } x=a \\
               f^{v} (a)=0 \rightarrow
                 \begin{cases}
                 ...
                 \end{cases}
              \end{cases}
         \end{cases}
    \end{cases}
    \end{align}


En general:

si $n$ és la primera derivada (després de la segona) no nul.la en $x=a$: $f^{n}(a)\ne 0 $ llavors:

* Si $n$ és imparell **$a$ és punt d'inflexió**
* Si $n$ és parell: **$a$ NO és punt d'inflexió** (la funció serà còncava o convexa en aquest punt).  

La funció $f(x)=x^3$ de l'exemple anterior té doncs un punt d'inflexió convex-còncau en $x=0$, ja que $f^{\prime \prime \prime} (x)=6 \ne 0$ és la primera derivada diferent de zero i té índex imparell.



##Aplicacions al càlcul de límits

El [Teorema de Cauchy](http://mdosil.cat/mates2batcientific/temes/funcions/#teorema-de-cauchy) ens servirà per a calcular límits amb dues indeterminacions concretes que abans no podíem calcular. Anem a veure-ho seguidament.

###Regla de l'Hôpital pel cas $\frac{0}{0}$

Considerem dues funcions $f(x)$ i $g(x)$ contínues i derivables en un entorn del punt $x=a$ de radi $r$: $E_a(r)$ que a més compleixen les condicions següents:

* $f(a)=g(a)=0 \Rightarrow \lim_{x\to a} \frac{f(x)}{g(x)}=\frac{0}{0}$ (IND)
* $g^\prime(x) \ne 0$ per qualsevol $x$ de l'entorn: $\forall x \in E_a(r)$ i $x \ne a$
* Existeix el límit $\lim_{x\to a} \frac{f^\prime(x)}{g^\prime(x)}$.




Amb aquestes condicions es pot [demostrar](https://ca.wikipedia.org/wiki/Regla_de_L%27Hôpital#Demostraci.C3.B3) que aquest el $\lim_{x\to a} \frac{f(x)}{g(x)}$ existeix i coincideix amb el límit del quocient de derivades:

$$
\bbox[5px,border:2px solid black] {\lim_{x\to a}\frac{f(x)}{g(x)}=\lim_{x\to a} \frac{f^\prime(x)}{g^\prime(x)}}
$$

**Exemple 4**

Calcula el límit:

$$\lim_{x\to 0} \frac{\ln(\cos 3x)}{\ln (\cos 2x)}=\frac{0}{0} IND$$

Apliquem l'Hôpital ja que $f(0)=g(0)=0$ on $f(x)=\ln(\cos 3x)$ i $g(x)=\ln (\cos 2x)$. Aquestes dues funcions són contínues i derivables en tot el seu domini. Per tant:

$$\lim_{x\to 0} \frac{\ln(\cos 3x)}{\ln (\cos 2x)} = \lim_{x \to 0} \frac{\frac{-3\sin 3x}{\cos 3x}}{\frac{-2\sin 2x}{\cos 2x}}=\lim_{x \to 0} \frac{3 \sin 3x \cdot \cos 2x}{2 \cos 3x \cdot \sin 2x}=\lim_{x \to 0} \frac{3 \tan 3x}{2 \tan 2x }=\frac{0}{0}$$

Tornem a aplicar la regla de l'Hôpital una segona vegada i tenim que:

$$\lim_{x\to 0} \frac{\ln(\cos 3x)}{\ln (\cos 2x)} = \lim_{x\to 0} \frac{3(1+\tan^2 3x)\cdot 3}{2(1+\tan^2 2x)\cdot 2}=\frac{9}{4}$$

###Regla de l'Hôpital pel cas $\frac{\infty}{\infty}$

De la mateixa manera, si seguim els mateixos passos que per la indeterminació $\frac{0}{0}$ podem calcular el límit del quocient de dues funcions on els límits individuals de cadascuna tendeixen a infinit:

Considerem dues funcions $f(x)$ i $g(x)$ contínues i derivables en un entorn del punt $x=a$ de radi $r$: $E_a(r)$ que a més compleixen les condicions següents:

* $ \lim_{x\to a} f(x)=\infty   \mbox{ i } \lim_{x\to a} g(x)=\infty \Rightarrow \lim_{x\to a} \frac{f(x)}{g(x)}=\frac{\infty}{\infty}$ (IND)
* $g^\prime(x) \ne 0$ per qualsevol $x$ de l'entorn: $\forall x \in E_a(r)$ i $x \ne a$
* Existeix el límit $\lim_{x\to a} \frac{f^\prime(x)}{g^\prime(x)}$.




Amb aquestes condicions es pot [demostrar](https://ca.wikipedia.org/wiki/Regla_de_L%27Hôpital#Demostraci.C3.B3) que aquest el $\lim_{x\to a} \frac{f(x)}{g(x)}$ existeix i coincideix amb el límit del quocient de derivades:

$$
\bbox[5px,border:2px solid black] {\lim_{x\to a}\frac{f(x)}{g(x)}=\lim_{x\to a} \frac{f^\prime(x)}{g^\prime(x)}}
$$

**Exemple 5**

Calcula el límit:

$$\lim_{x\to 1^+} \frac{ln (x^2-1)}{ln(x-1)}=\frac{\infty}{\infty} IND$$

Sabem que les dues funcións són contínues i derivables en un entorn petit de $x=1$ per tant, podem aplicar la regla de l'Hôpital per a calcular el límit:

$$\lim_{x\to 1^+} \frac{ln (x^2-1)}{ln(x-1)}=\lim_{x\to 1^+} \frac{\frac{2x}{x^2-1}}{\frac{1}{x-1}}=\lim_{x\to 1^+} \frac{ 2x(x-1)}{(x-1)(x+1)}=1$$

###Aplicació de la regla de l'Hôpital a altres indeterminacions

La regla també s'aplica amb altres indeterminacions ($0 \cdot \infty$, $\infty-\infty$, $1^\infty$,  $0^0$, $\infty ^\infty$ ), però primer caldrà transformar les expressions dels límits algebraicament. Anem a veure cada cas.

1. Indeterminació $0 \cdot \infty \rightarrow f(x) \cdot g(x)= \frac{f(x)}{\frac{1}{g(x)}}=\frac{g(x)}{\frac{1}{f(x)}}$
2. Indeterminació $\infty - \infty \rightarrow f(x) - g(x)= \frac{\frac{1}{g(x)}-\frac{1}{f(x)}}{\frac{1}{f(x)g(x)}}$
3. Indeterminacions $1^\infty$,  $0^0$ i $\infty ^\infty \rightarrow$ Caldrà aplicar logaritmes a banda i banda abans de calcular el límit, per a transformar-ho en una indeterminació del tipus $0 \cdot \infty$ i aplicar el primer procediment.


**Exemple 6**

\begin{align}
\lim_{x\to 1^+} (x-1)ln(x-1) &=0 \cdot (-\infty)=\lim_{x\to 1^+} \frac{ln(x-1)}{\frac{1}{x-1}}=\frac{\infty}{\infty}\xrightarrow[]{Hôpital}\\
&=lim_{x\to 1^+} \frac{\frac{1}{x-1}}{\frac{-1}{(x-1)^2}}=lim_{x\to 1^+} \frac{-(x-1)^2}{x-1}=0
\end{align}

**Exemple 7**

\begin{align}
\lim_{x\to 0} \Big(\frac{1}{x^2}-\frac{1}{\sin x}\Big) &=(\infty-\infty)=\lim_{x\to 0} \frac{\sin x-x^2}{x^2 \sin x}=\frac{0}{0}\xrightarrow[]{Hôpital}\\
&=lim_{x\to 0} \frac{\cos x -2x}{x^2 \cos x +2 x\sin x}=\frac{1}{0}=\infty
\end{align}

Cal trobar ara el signe de l'infinit:

\begin{align}
\mbox{Signe }\infty \rightarrow
\begin{cases} \lim_{x\to 0^+} (x^2 \cos x+ 2x \sin x)=0^+\\
\lim_{x\to 0^-} (x^2 \cos x+ 2x \sin x)=0^+
    \end{cases}
    \end{align}

Per tant:

$$\lim_{x\to 0} \Big(\frac{1}{x^2}-\frac{1}{\sin x}\Big)=+\infty$$

**Exemple 8**

$$\lim_{x\to 0} (\sin x)^x=0^0$$

Fem un canvi de variable i apliquem logaritmes a banda i banda:

\begin{align}
\lim_{x\to 0} (\sin x)^x &=  a\\
ln \Big( \lim_{x\to 0} (\sin x)^x \Big) &= ln a\\
\lim_{x\to 0} ln \Big((\sin x)^x \Big) &= ln a\\
\lim_{x\to 0} x \cdot ( ln  (\sin x) ) &= 0 \cdot (-\infty)\\
\end{align}

Fem una transformació algebraica a l'expressió de la funció per poder aplicar la regla de l'Hôpital:

\begin{align}
\lim_{x\to 0} x \cdot ( ln (\sin x)) &=  \lim_{x\to 0} \frac{ln (\sin x)}{\frac{1}{x}}=\frac{\infty}{\infty}\xrightarrow[]{Hôpital}\\
&=\lim_{x\to 0}\frac{\frac{1}{\sin x}\cdot \cos x}{\frac{-1}{x^2}}=\lim_{x\to 0}\frac{-x^2 \cos x}{\sin x}=\frac{0}{0}\xrightarrow[]{Hôpital}\\
&=\lim_{x\to 0}\frac{-2x \cos x+x^2 \sin x}{\cos x}=\frac{0}{1}=0
\end{align}

Ara ens cal desfer el canvi de variable per acabar d'avaluar el límit:

$$ln a = 0 \rightarrow a=e^0=1$$

Per tant:

$$\lim_{x\to 0} (\sin x)^x=1$$
