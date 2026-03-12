---
title: "Low Tech High Life: Emacs magia y liberación"
date: 2026-03-12
draft: false
description: "Emacs es un editor de textos, una reliquia de un mundo mágico estas son palabras de amor a una herramienta que amo. Columna emitida 2025-11-29"
rss_description: "Emacs es un editor de textos, una reliquia de un mundo mágico estas son palabras de amor a una herramienta que amo. Columna emitida 2025-11-29"
tags: ["radio", "emacs", "magia","herramientas"]
categories: ["lento es normal"]
featureimage: featured.png
audio:
  - "https://archive.org/download/lento-es-normal-miercoles-29-10-25/LENTO_ES_NORMAL-MIERCOLES-29-10-25.mp3"
---

{{< archiveaudio id="lento-es-normal-miercoles-29-10-25" >}}

Emacs es un editor de textos, una reliquia de un mundo mágico.
Vale la pena preguntarnos Qué herramientas elegimos usar en nuestro día a día. Estas son palabras de amor a una herramienta que amo.

<!--more-->

Podcast disponible en:

<div style="display:flex;gap:1rem;flex-wrap:wrap;justify-content:center;align-items:center;">
<a href="https://archive.org/details/@amaciel" rel="noopener" target="_blank">
  <img class="nozoom" src="/images/internet-archive-podcast-badge.svg" alt="Escuchalo en Internet Archive" width="165" height="40">
</a> | 

<a href="https://open.spotify.com/show/5hJVg8ZiQIfBk8hHxNlpOS" rel="noopener" target="_blank">
  <img class="nozoom" src="/images/spotify-podcast-badge.svg" alt="Escuchalo en Spotify" width="165" height="40">
</a> | 

<a href="/media/lento_es_normal/index.rss" rel="noopener" target="_blank">
  <img class="nozoom" src="/images/rss-podcast-badge.svg" alt="Conectalo a tu reproductor (RSS)" width="165" height="40">
</a>
</div>



Me gusta conectar textos. Tender puentes entre personas e ideas. Me gusta [421](https://www.421.news/) porque se mete entre otras lecturas y pone en juego pasiones, ideas y temores que me convocan. Y además, nos permite interactuar, y al menos responder,  o iniciar un diálogo que puede florecer o no. Pero que esta dado. Abierto. 
El artículo [Low Tech Hig Life](https://www.421.news/low-tech-high-life-cottagecore-cyberpunk/) da mucha tela para cortar. Una de ellas: Qué herramientas elegimos usar en nuestro día a día.

En mi caso, necesito una para editar y leer textos. Ya sea para programar algo o para volcar mis ideas cuando no tengo un papel a mono. Y nada más low tech para esto que el texto plano. Nada más high life que Emacs.

Quiero compartirles extractos de un sensayo titulado  [bare metal (the emacs essay) de Wax Banks](https://waxbanks.wordpress.com/2025/08/01/bare-metal-the-emacs-essay/). Sería algo así como Fierro desnudo (El ensayo de emacs)

Este texto puso en palabras mucho de lo que pienso, o más bien siento con mi editor de texto favorito.

Además dialoga directamente con lo que Juan expone en su artículo y con lo que algunos venimos tratando de recuperar. Un espacio de soberanía cognitiva.

Lo que lees voy a leer a continuación es una carta de amor, amor por todo lo que la programación tiene para ofrecernos. 

Programar es mucho más que un trabajo para algunos de nosotros, es más que hacer algo que nos sirva. Programar es dominar la magia de las ideas abstractas convirtiendolas en cosas que podemos manipular para crear.

Esta es una carta de amor hecha de recortes y sentimientos. Un collage que quiere develar la pasión por herramientas que nos liberan. La profunda conexión que algunos encontramos entre los sistemas que regulan nuestros días y su raíz olvidada/negada transformadora. 

### Breve intro

> Emacs tiene aproximadamente 50 años y se nota, y los usuarios que llegan a Emacs desde programas comerciales modernos son como habitantes de departamentos urbanos obligados a desenchufar sus microondas y descubrir el fuego. Los microondas hacen las cosas difíciles más fáciles, las cosas lentas más rápidas y los malos trabajos mejores, pero sin otras herramientas no pueden hacer una buena comida; además, cuando suban los mares y se apaguen las luces, los microondas serán inútiles excepto como cuchas para mascotas pequeñas. El fuego permanece.
> No se puede gobernar sin fuego.


> Usar Emacs es interactuar con un sistema distinto a cualquier otro programa de capacidades similares: uno construido alrededor de la introspección —autoexamen, el editor exponiendo y editando su propio código— y un grado de extensibilidad inigualable.

> Emacs es una obra filosófica encarnada: una forma de vivir libre (a la que solo le falta un editor de texto decente).

> Emacs articula una filosofía de libertad que sostiene que una persona no es verdaderamente libre a menos que tenga privacidad total y control total sobre sus herramientas. Por eso todo Emacs está abierto al examen y la introspección hasta los mismos fierro, su base, su código C de más bajo nivel. A pesar de la complejidad de la herramienta y el entorno computacional, nada se le esconde al usuario. El programa fue construido específicamente para permitir esa introspección; para eso está, no para editar texto —que lo hace bien— sino para otorgar (ejercer) control sobre la computación, exactamente lo opuesto a las convenciones de los &rsquo;jardines vallados&rsquo; actuales. (Probá conseguir repuestos alternativos para tu Tesla.)

---

### seguridad a cambio de libertad.

> Es un programa que está perfectamente alineado en el espíritu de sus orígenes en el movimiento de los 70 por de una computación personal liberadora, la creación y difusión de herramientas para aumentar la salud y capacidad humana en lugar de extraernos dólares publicitarios. (Silicon Valley simplemente abandonó este ethos, que es una de las razones por las que Richard Stallman, el creador de Emacs, es ridiculizado por estos caretas.)

> El objetivo del programa es brindar, posibilitar, una experiencia emancipatoria de computación autónoma. Las mentes son lo que los cuerpos hacen y las herramientas extienden la mente-cuerpo: el control de las herramientas es libertad.

> No estás realmente usando el programa hasta que empezás a pensar como él piensa —momento en el cual se vuelve difícil imaginar usar otra cosa a menos que te obliguen o estés obligado&hellip;
> Emacs logra tanto articular un sistema de creencias como ser, fuera de joda, una herramienta poderosa que es un placer usar y dominar.

### Sistema mágico

> &hellip; por supuesto que deberíamos mirar a Emacs como una especie de sistema mágico, todo un reino alternativo que requiere trabajo para que tenga sentido —y una vez que tiene sentido puede hacer cualquier cosa. Podés usarlo para editar archivos de texto, incluso en lenguajes humanos, pero eso sería como &rsquo;usar magia&rsquo; para &rsquo;hacer un hechizo de amor&rsquo;. Los hechizos  son efectos secundarios de la transformación imaginativa del mago, carajo,  francamente si lo que querés sacar de la indagación mágica es hacer que alguien se enamore de vos entonces hay mejores herramientas ahí afuera, como por ejemplo la conversación atenta y curiosa. Lleva un montón de trabajo hacer que Emacs &rsquo;simplemente funcione&rsquo;, pero así debe ser: aprender Emacs —como aprender Lisp o latín, tantra o tarantela— no resuelve problemas en sí mismo, te deja ver nuevas formas de resolver problemas.

> Ya nadie habla latín, pero casi todos en Occidente hablan algún idioma al que aprender latín te da acceso. Meditar no te va a &rsquo;hacer mas tranquilo&rsquo;, pero podría ayudarte a entender cómo lograrlo. El poder de la herramienta es que sos vos quien se vuelve más poderoso, es decir, más listo/capaz de asumir responsabilidad auténtica por la creación, es decir, más libre.


> Todos los hechizos se lanzan sobre quien los lanza.
> La magia no funciona, nos seguimos diciendo, pero funciona. Para decirlo con más precisión: una vez que tenés tus archivos de configuración (conciencia, sistema mágico, caja de herramientas) como los querés, podés hacer todas las cosas que te propusiste hacer desde un principio.

> De ahí la diferencia entre la industria de la &rsquo;computadora personal&rsquo; y el movimiento de la &rsquo;computación personal&rsquo;, la primera es sobre comprar y usar herramientas, la segunda sobre transformar y expandir el yo a través del uso de herramientas, realizando el potencial humano&hellip; y siendo, como &rsquo;efecto secundario&rsquo;, menos propenso a comprar bienes de consumo caros de los depredadores ordinarios. ¿Por qué pensás que mataron el movimiento&hellip;?

### Mundo y Mundo

> Nuestro ruinoso mundo nuevo requiere algo distinto, una amenabilidad &rsquo;amigable para el consumidor&rsquo; y a la medida de Mercados Extranjeros. Requiere que todo tenga  un Modo tutorial, resúmenes. No hay mercados para el misterio; no hay tiempo para soñar despierto, eso pertenece a un viejo mundo menos productivo.
> Así vivimos:
> Queriendo que funcione apenas lo saco de la caja.
> - Queriendo latencia cero.
> - Queriendo identificarme con el héroe. Estando seguros de que el autor también lo hace.
> - Decime qué me vas a decir, después decímelo, después decime qué me dijiste.
> - Guiáme paso a paso por el trabajo, en una clase autodirigida.
> - Siiií, necesito  eso en una hora, gracias.
> &hellip;todo lo cual es exactamente lo opuesto de la imprecisión fecunda de la magia, como el porno es lo opuesto del erotismo y &rsquo;spoiler&rsquo; es lo opuesto del &rsquo;relato&rsquo; (asombro)

> Las herramientas que te dejan hacer un trabajo más difícil y mejor son una bendición; las que hacen la vida más fácil pero peor son la otra cosa, incluso si nos criaron mal y aprendimos a valorarlas.

> Abrirse camino más allá de la satisfacción fácil hacia la realización profunda significa rechazar la manía por la facilidad y la conveniencia en el núcleo de nuestra religión de estado consumista secular —y abrazar, no sin riesgo, una realidad alternativa fuera del consenso.

### Emacs

> Emacs representa una apuesta que no dio resultado, por un futuro que nunca, jamás se va a permitir que llegue. Encarna la creencia encantadora pero equivocada de que crear herramientas para hacer a la gente más libre va a iniciar un movimiento hacia la libertad. Si lo hubieran hecho punks en lugar de hippies —en lugar de científicos e ingenieros viviendo en una esperanza meritocrática equivocada— quizás el movimiento que representa estaría en posición de exigir en lugar de recordar.

> Cada vez que me siento en mi computadora y abro Emacs entro en el futuro desvanecido de un pasado desvanecido en lugar de al futuro, y se me otorga acceso a un poder inigualable, y me rompe el puto corazón.



- imagen: Senshi, preparando la comida, tomandose tiempos para descubrise cocinando.

