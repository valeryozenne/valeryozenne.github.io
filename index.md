---
layout: index
special_keywords: ["Imagerie par résonance magnétique", "Mesure de temperature non invasive", "Modèle numérique thermique", "Aide à la décision"]
paragraphs:
  - title: "Imagerie interventionnelle et cartographie thermique par IRM"
    content: "
    <p>Les thermoablations sont des procédures médicales couramment utilisées pour détruire des tissus pathologiques via un dépôt d’énergie localisé.</p> 
    
    <p>Différents dispositifs médicaux mini-invasifs tels que le laser, la radiofréquence ou les micro-ondes, ou des dispositifs non-invasifs comme les ultrasons de haute intensité peuvent être utilisés. Deux thérapies sont principalement concernées: l'oncologie pour le traitement des tumeurs cancéreuses et la cardiologie pour l'ablation des tissus cardiaques arythmogènes responsables des arythmies cardiaques.</p>

    <p> Néanmoins, de nombreuses procédures sont réalisées sans visualisation du champ thermique et ne permettent pas d'optimiser le dépot d'énergie pour atteindre les marges souhaitées. </p> 
    
    <p> L'imagerie de température par IRM nommé aussi thermométrie permet de quantifier en temps réel et de manière volumétrique le champ thermique pendant l'intervention. </p>
    
    <p> Mes travaux actuels proposent une refonte de ces approches en couplant la mesure expérimentale par IRM avec des modèles physiques thermiques afin d'augmenter la précision et de fournir au praticien des mesures de température inégalées en terme de résolution spatiale et temporelle. Ces courbes sont cruciales pour quantifier les marges d'ablation et aider à la décision lors de la procédure. </p>"    

    keywords: ["Imagerie thermique", "Thermo-Ablation", "Thérapie guidée par l'image", "Analyse en temps-réel", "Dispositifs médicaux"]
    links: "/thermoablation/"

  - title: "Thermorégulation, hyperthermie et cartographie thermique par IRM"
    content: "<p>L’élévation des températures représente un enjeu de santé publique important avec un nombre décès imputables à la chaleur croissant sur les deux dernières décennies. Malgré ce constat, les autorités publiques soulignent le manque de données expérimentales et d’études cliniques pour 's’adosser à un socle de connaissances scientifiques et techniques, afin de pouvoir mieux informer et prévenir les publics vulnérables'.</p>

    <p>En milieu chaud et humide, la saturation des mécanismes de thermolyse peut conduire à une élévation de température corporelle, appelée hyperthermie. Le coup de chaleur, stade pathologique critique, implique une mortalité après admission en réanimation notable si liée à l’effort et acrrue si elle résulte d'une exposition passive à une chaleur ambiante. La prise en charge est limitée par le manque de compréhension des mécanismes de thermorégulation.</p>

    <p> Mes travaux actuels explorent de nouvelles prises en charges environnementales et pharmacologiques du coup de chaleur. Pour atteindre ces objectifs, de nouvelles techniques IRM de cartographie thermique sans contact sont développées pour mesurer les changements de T°C faibles, lents et diffus au cours de longues périodes de stress thermique.</p>"

    keywords: ["Thermorégulation", "Hyperthermie", "Coup de chaleur"]
    links: "/hyperthermie/"

  - title: "Etude de l'architecture cardiaque par IRM de diffusion"
    content: "<p> Les maladies cardiaques d'origine électrique représentent un problème majeur de santé publique avec près de 350 000 morts subites par an en Europe dont 50 000 en France. Dans la moitié des cas, elles sont la conséquence de perturbations du rythme cardiaque appelées fibrillations ventriculaires (FV) qui conduisent rapidement à la mort en l'absence de réanimation. Ces évènements
    peuvent survenir chez des patients en bonne santé sans cardiopathie ou chez des patients présentant une prédisposition génétique. Au cours des 20 dernières années, des efforts considérables ont été consacrés à la recherche de marqueurs électrocardiographiques ou d'imagerie et de causes génétiques chez les survivants. Récemment, l'équipe clinique du CHU-Bordeaux a réussi à visualiser une signature
    électrique atypique chez des patients sans altération structurelle visible macroscopiquement ou connue [Haïssaguerre 2018, Haissaguerre 2022]. Cette signature indique généralement une perte de cohérence électrique survenant localement dans un petit volume de tissu. Le mécanisme le plus probable, impliquant ces régions anatomiques critiques responsables de la mort subite, serait la présence de remodelage structurel du tissu cardiaque à l'échelle microscopique. Ce mécanisme et la compréhension de la dynamique de l'arythmie restent inconnu à ce jour</p>

    <p> Mes travaux de recherche s'appuie sur deux programmes de dons d'organes en cours (coordination CHU-Bordeaux - IHU Liryc - l'agence de Biomédecine) et visent grâce à l'utilisation d'IRM à haut champs à améliorer notre compréhension de microstructure cardiaque </p>"
    keywords: [ "Architecture cardiaque", "IRM de diffusion" , "Arythmie",]
    links: /microstructure/
---

Je suis chargé de recherche au [CNRS](https://www.cnrs.fr/fr), et rattaché au [Centre de Résonance Magnétique des Systèmes Biologiques](https://www.rmsb.u-bordeaux.fr/fr/) à Bordeaux. 

Mes travaux portent sur le développement de nouvelles méthodes d’imagerie thermique par IRM. Mon cœur de métier concerne le développement d’algorithmes de reconstruction ou de traitements d’images innovants pour transformer le signal brut IRM en information de température interprétable, le tout avec une contrainte de temps réel.

Mots clés:
<div class="keywords">
  {% for skw in page.special_keywords %}
    <span class="kww">{{ skw }}</span>
  {% endfor %}
</div>

<br> 

<a href="https://translate.google.com/translate?sl=fr&tl=en&u={{ site.url }}{{ page.url }}" target="_blank">View the page in English 🇬🇧</a>

<br> <!-- Ajoute une ligne vide après les mots-clés -->

# Projects
{% for paragraph in page.paragraphs %}
  <h2 class="subheading">{{ paragraph.title }}</h2>

  {{ paragraph.content | markdownify }} 

  <div class="keywords">
    {% for kw in paragraph.keywords %}
      {% if forloop.parentloop.first %}
        <span class="kwg">{{ kw }}</span>
      {% elsif forloop.parentloop.last %}
        <span class="kwb">{{ kw }}</span>  
      {% else %}
        <span class="kwr">{{ kw }}</span>
      {% endif %}
    {% endfor %}
  </div>

  <br> <!-- Ajoute une ligne vide après les mots-clés -->
  <div class="paragraph-links">
    <a href="{{ paragraph.links }}">En savoir plus →</a>
  </div>

  <br> <!-- Ajoute une ligne vide après les mots-clés -->

{% endfor %}

# Latest articles

{% bibliography --max 5 --sort %}

# Selected articles
{% bibliography --query @*[pages=2194595] %}
{% bibliography --query @*[pages=116236] %}
{% bibliography --query @*[volume=77]  %}
{% bibliography --query @*[pages=78] %}
{% bibliography --query @*[pages=H936--H952] %}

# Latest News
<ul class="post-list">
  {% for post in site.posts limit:2 %}
  {% if post.type == "news" %}
  <li>
    <h4>{{ post.title }}
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h4>
    {{ post.content }}
  </li>
  {% endif %}
  {% endfor %}
</ul>

<!---
# News

<ul>
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%B %Y" %}
  {% if currentdate != date %}
    <li id="y{{currentdate}}">{{ currentdate }}</li>
    {% assign date = currentdate %} 
  {% endif %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
-->
<!---
# News


<ul class="post-list">
  {% for post in site.posts %}
  {% if post.type == "news" %}
  <li>
    <h2>{{ post.title }}
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h2>
    {{ post.content }}
  </li>
  {% endif %}
  {% endfor %}
</ul>
-->


<!--
I’m a researcher in medical imaging in a [CNRS](https://www.cnrs.fr/fr/page-daccueil) laboratory, the "Centre de Résonance Magnétique des Systèmes Biologiques" (Bordeaux, France).
-->

<!--
Mots clés: Imagerie par résonance magnétique, Mesure de temperature non invasive, Thermoablation, Modèles numériques thermique, Dispositifs Médicaux.
-->