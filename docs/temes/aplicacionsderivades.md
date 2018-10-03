#Tema 3: Estudi de les característiques d'una funció. Problemes d'optimització

##Representació gràfica d'una funció

En aquest apartat aprendrem a representar una funció seguint uns passos concrets i analitzarem totes les seves característiques. Per a fer-ho, partirem d'un exemple concret:

$$f(x)=\frac{x^2-2x+2}{x-1}$$

### Domini

El domini dependrà de cada funció. Si voleu fer un repàs sobre dominis dels diferents tipus de funcions, podeu repassar els [apunts de l'any passat](http://mdosil.cat/mates1batcientific/temes/funcions/#domini-duna-funcio).

En el cas del nostre exemple, el domini són tots els nombres reals menys aquells punts que anul.len el denominador:

$$D=\mathbb{R}-{1}$$

### Signe de la funció

Ens interessa agafar el pla cartesià i ratllar aquelles zones a les quals no hi hagi funció. Per fer-ho, ens caldrà trobar els zeros de la funció i ajuntar-los amb els punts que __no són del domini__ i dividir el pla en sectors. Llavors prendrem un punt de cada un dels sectors i mirarem el signe de la funció. Si la funció és contínua, podrem assegurar que el signe es manté en cada regió.

Pel que fa a la nostra funció:

Per trobar-ne els zeros cal resoldre l'equació:

$$x^2-2x+2=0 \rightarrow x= \frac{2 \pm \sqrt{4-8}}{2}= \nexists$$

Com que la funció no s'anul.la mai, només cal que dividim el pla en dos intervals de $x$ i mirem quin signe hi té la funció allà:

\begin{align}
(-\infty, 1) &\rightarrow f(0)<0 \\
(1, +\infty) &\rightarrow f(2)>0 \\
  \end{align}

Per tant, començarem la nostra representació gràfica assenyalant el punt que no és del domini i la regió on no hi ha funció (pintada en blau):



<iframe scrolling="no" title="signe d'una funció" src="https://www.geogebra.org/material/iframe/id/x8XEmYzc/width/513/height/440/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="513px" height="440px" style="border:0px;"> </iframe>

### Simetries

A vegades és útil d'estudiar les simetries de les funcions, ja que si una funció és simètrica només ens cal representar-ne un tros. Anem a recordar el dos tipus de simetries que existeixen:

* Una funció és __parell__ si és simètrica respecte l'eix de les ordenades. Algebraicament vol dir que compleix: $f(x)=f(-x)$. Un exemple de funció parell és: $f(x)=x^2$. A la pràctica, si pleguem la funció per l'eix de les $y$ les dues parts coincideixen.

* Una funció és __senar__ si és simètrica respecte l'origen de coordenades i es compleix que: $f(x)=-f(-x)$. Un exemple n'és $f(x)=x^3$. A la pràctica vol dir que si pleguem primer la funció per l'eix de les $x$ i després per l'eix de les $y$ les branques de la gràfica coincideixen.

En el cas del nostre exemple:

\begin{align}
f(x) &\ne f(-x) \\
f(x) &\ne - f(-x) \\
  \end{align}

Per tant, no hi ha simetries.

###Assímptotes

El [curs passat](http://mdosil.cat/mates1batcientific/temes/limits/#discontinuitat-assimptotica) vam parlar de les assímptotes horitzontals i verticals d'una funció molt breument. Una funció qualsevol pot tenir 3 tipus d'assímptotes:

* __Verticals__. Això passa si al calcular el límit quan ens acostem a cert valor de $x$ el resultat és infinit. Calculem aquests límits amb punts que no pertanyen al domimi de la funció. Si $a$ no pertany al domini de $f(x)$ llavors:

$$\lim_{x\to a }f(x)=\pm \infty$$

* __Horitzontals__. Per trobar les assímptotes horitzontals cal mirar què val el límit de la funció a $+\infty$ i a $-\infty$:


\begin{align}
\mbox{ si } \lim_{x\to +\infty}f(x)=a &\rightarrow \mbox{ en }y=a \mbox{ hi ha una assímptota horitzontal per la dreta}  \\
\mbox{ si } \lim_{x\to -\infty}f(x)=a &\rightarrow \mbox{ en }y=a \mbox{ hi ha una assímptota horitzontal per l'esquerra}  \\
  \end{align}

* __Oblícues__. Una assímptota oblícua tindrà l'equació d'una recta: $y=mx+n$. Hi ha assímptotes oblícues sempre que no n'hi hagi d'horitzontals. Ens caldrà doncs, trobar els paràmetres $m$ i $n$ de la manera següent:

\begin{align}
m&= \lim_{x\to +\infty} \frac{f(x)}{x}\\
 n&= \lim_{x\to +\infty} (f(x)-mx)\\
  \end{align}

Tornem a la funció $f(x)=\frac{x^2-2x+2}{x-1}$:

* Assímptotes verticals. És possible que en tingui perquè el punt $x=1$ no pertany al domini. Anem a veure-ho:

$$\lim_{x\to 1} \frac{x^2-2x+2}{x-1}=\frac{1}{0}=\infty$$

Caldrà veure ara el signe d'aquest infinit:

\begin{align}
\lim_{x\to 1^-} \frac{x^2-2x+2}{x-1}&=\frac{1}{0^-}=-\infty\\
\lim_{x\to 1^+} \frac{x^2-2x+2}{x-1}&=\frac{1}{0^+}=+\infty\\
\end{align}

Per tant, en x=1 té una assímptota vertical per l'esquerra cap a $-\infty$ i una vertical per la dreta cap a $+\infty$

* Assímptotes horitzonals:

\begin{align}
\lim_{x\to +\infty} \frac{x^2-2x+2}{x-1}&=+\infty\\
\lim_{x\to -\infty} \frac{x^2-2x+2}{x-1}&=-\infty\\
  \end{align}

  No hi ha assímptotes horitzontals.

* Assímptotes oblícues:

\begin{align}
m&=\lim_{x\to +\infty} \frac{f(x)}{x}=\lim_{x\to +\infty} \Big(\frac{x^2-2x+2}{x^2-x}\Big)=1\\
n&=\lim_{x\to +\infty} \Big(f(x)-mx \Big)=\lim_{x\to +\infty} \Big(\frac{x^2-2x+2}{x-1}-x\Big)=\lim_{x\to +\infty} \Big(\frac{x^2-2x+2-x(x-1)}{x-1}\Big)=\lim_{x\to +\infty}\frac{-x+2}{x-1}=-1\\
  \end{align}

Hi ha una assímptota oblícua en $y=x-1$.

Anem a dibuixar la recta de l'assímptota oblícua:

<iframe scrolling="no" title="assímptotes d'una funció" src="https://www.geogebra.org/material/iframe/id/MxRupWf6/width/513/height/440/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="513px" height="440px" style="border:0px;"> </iframe>

###Creixement i decreixement

Vèiem en el [tema anterior](http://mdosil.cat/mates2batcientific/temes/funcions/#creixement-i-decreixement) que el creixement i decreixement d'una funció el determinava el signe de la 1a derivada. El procediment serà el següent:

* Calculem la derivada de la funció
* Busquem els punts pels quals $f^\prime (x)=0$
* Partim les $x$ en diferents intervals, agafant els punts que no són del domini i els zeros de la derivada primera.
* Calculem el signe de la derivada en cadascun dels intervals per saber si la funció creix o decreix (si $f^\prime (x)>0$ la funció serà creixent en l'interval, en cas contrari, decreixent).

Per la nostra funció $f(x)=\frac{x^2-2x+2}{x-1}$:

$$f^\prime(x)=\frac{x^2-2x}{(x-1)^2}\rightarrow \frac{x^2-2x}{(x-1)^2}=0 \rightarrow x_1=0, x_2=2$$

Hem trobat 2 punts singulars on la derivada s'anul.la. Agafem aquests punts, juntament amb el punt que no era del domini ($x=1$) i construïm 4 intervals. A cadascun d'ells triem un punt i comprovem el signe de la 1a derivada:

\begin{align}
(-\infty,0)&\rightarrow f^\prime(-1)>0\rightarrow f(x) \mbox{ és creixent}\\
(0,1)&\rightarrow f^\prime(\frac{1}{2})<0\rightarrow f(x) \mbox{ és decreixent}\\
(1,2)&\rightarrow f^\prime(\frac{3}{2})<0\rightarrow f(x) \mbox{ és decreixent}\\
(2,+\infty)&\rightarrow f^\prime(3)>0\rightarrow f(x) \mbox{ és creixent}\\
  \end{align}


###Extrems locals

Per trobar els màxims i mínims locals, [tal i com vam veure el tema passat](http://mdosil.cat/mates2batcientific/temes/funcions/#maxims-i-minims-locals) ens cal agafar els punts singulars o estacionaris i veure el signe de la segona derivada. Si la segona derivada en aquells punts és negativa, tindrem un màxim local en el punt, si és positiva, tindrem un mínim.

Si prenem el nostre exemple, els punts singulars eren $x_1=0$, $x_2=2$:



\begin{align}
f^{\prime \prime}(x)=...=\frac{2}{(x-1)^3}\\
f^{\prime \prime}(0)<0 \rightarrow \mbox{ màxim local en el punt} (0, -2)\\
f^{\prime \prime}(2)>0 \rightarrow \mbox{ mínim local en el punt} (2, 2)\\
  \end{align}

<iframe scrolling="no" title="màxims i mínims d'una funció" src="https://www.geogebra.org/material/iframe/id/qkBtv2mD/width/513/height/440/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="513px" height="440px" style="border:0px;"> </iframe>

###Punts d'inflexió

[Són aquells pels quals es compleix:](http://mdosil.cat/mates2batcientific/temes/funcions/#punts-dinflexio) $f^{\prime \prime}(x)=0$.

En el cas del nostre exemple, no hi ha cap punt on la segona derivada s'anul.li, per tant, la nostra funció no té punts d'inflexió.

###Concavitat i convexitat

[Tal i com vam veure](http://mdosil.cat/mates2batcientific/temes/funcions/#concavitat-i-convexitat) ens caldrà estudiar el signe e la segona derivada. Caldrà dividir les $x$ en intervals, agafant els punts que no són del domini i els punts d'inflexió si ni hagués. En cadascun dels intervals caldrà estudiar el signe de la segona derivada.

Pel nostre cas:

\begin{align}
(-\infty,1)&\rightarrow f^{\prime \prime}(0)<0\rightarrow f(x) \mbox{ és convexa en l'interval}\\
(1,+\infty)&\rightarrow f^{\prime \prime}(2)>0\rightarrow f(x) \mbox{ és cóncava en l'interval}\\
  \end{align}

###Gràfica de la funció

Amb totes les dades que hem anat obtenint dels passos anteriors, ja estem en disposició de dibuixar la funció. És possible que hàgim de buscar un parell de punts més per poder-la traçar amb més precisió, també.

<iframe scrolling="no" title="funció f(x)=(x^-2x+2)/(x-1)" src="https://www.geogebra.org/material/iframe/id/wWK3agWB/width/543/height/439/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="543px" height="439px" style="border:0px;"> </iframe>

##Problemes d'optimització

Els problemes d'optimització es treballen aquí perquè s'utilitza la derivada i les propietats de les funcions per a maximitzar o minimitzar una quantitat donada. [D'exemples n'hi ha molts](http://www.sangakoo.com/ca/temes/optimitzacio) i cada problema té les seves pròpies característiques. Tota manera, cal seguir un procediment ordenat de resolució:

1. Comprensió de l'enunciat i si cal dibuix esquemàtic (sobretot si el problema involucra quantitats geomètriques)
2. Determinació de les variables del problema
3. Planteig de la funció a optimitzar
4. Incorporació d'informació extra per a simplificar la funció a optimitzar
5. Derivar la funció a optimitzar respecte la variable corresponent i trobar el punt pel qual la funció es maximitza o minimitza (segons sigui el cas).
6. Interpretació del resultat i solució.

Intentarem seguir aquest esquema en l'exemple següent:

__Exemple 1__

Entre tots els cilindres de volum $4\pi$ trobeu el que suposi menys cost a l'hora de construir-lo.

1. Entenem que menys cost a l'hora de construir-lo vol dir que tingui la mínima superfície possible amb el mateix volum, que és $4\pi$. Anem a fer un dibuix esquemàtic:

    <iframe scrolling="no" title="cilindre" src="https://www.geogebra.org/material/iframe/id/rjbzB79s/width/489/height/413/border/888888/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="489px" height="413px" style="border:0px;"> </iframe>


2. Les variables del problema en aquest cas són el radi $R$ i l'alçada $H$.
3. La funció a optimitzar serà la despesa total de material a l'hora de construir-lo i això depèn de l'àrea total del cilindre:

    $$A(R,H)=2\pi R^2+2\pi R H$$

4. La nostra funció depèn de dues variables, però tenim una informació suplementària que ens dóna l'enunciat que fa que en puguem eliminar una. Sabem que el volum total del cilindre és $4\pi$. Per tant:

    \begin{align}
    V&=\pi R^2 H = 4\pi \rightarrow H=\frac{4}{R^2}\\
    A(R)&= 2 \pi R^2+ 2 \pi R \cdot \frac{4}{R^2}=2 \pi R^2+\frac{8\pi}{R}
    \end{align}

    I ara tenim que la funció a optimitzar només depèn d'un paràmetre, $R$.

5. Derivem la funció, igualem la primera derivada a zero i mirem per a quins valors la segona derivada és positiva (es tracta de __minimitzar__ la superfície):

    \begin{align}
    A^\prime(R)&= 4 \pi R-\frac{8\pi}{R^2}=\frac{4\pi R^3-8\pi}{R^2}\\
    A^\prime(R)&=0 \rightarrow 4\pi R^3-8\pi=0 \rightarrow ... \rightarrow R=\sqrt[3]{2}\\
    A^{\prime \prime} (R)&=\frac{12\pi R^2 \cdot R^2-2R(4\pi R^3-8\pi)}{R^4}=...=\frac{4\pi R^3+16 \pi}{R^3}\\
    A^{\prime \prime}(\sqrt[3]{2})&>0\rightarrow \mbox{ En } R=\sqrt[3]{2} \mbox{ hi ha un mínim local}
    \end{align}

    Substituïm i trobem el valor de l'alçada del cilindre per aquest radi:

    $$H=\frac{4}{R^2}=\frac{4}{\sqrt[3]{2^2}}=...=2\sqrt[3]{2}$$

6. El cilindre que minimitza l'àrea i que té volum $4\pi$ té dimensions: $H=2\sqrt[3]{2}$ i $R=\sqrt[3]{2}$
