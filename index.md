---
layout: index
special_keywords: ["Imagerie par résonance magnétique", "Mesure de temperature non invasive", "Modèle numérique thermique", "Aide à la décision"]
paragraphs:
  - title: "Imagerie interventionnelle et cartographie thermique par IRM"
    content: "
    Les thermoablations sont des procédures thérapeutiques couramment utilisées pour détruire des tissus pathologiques via un dépôt d’énergie localisé. 
    
    Néanmoins, de nombreuses procédures sont réalisées sans visualisation du champ thermique et ne permettent pas d'optimiser le dépot d'énergie pour atteindre les marges souhaitées. 
    
    L'imagerie de température par IRM nommé souvent thermométrie permet de quantifier en temps réel et de manière volumétrique le champ thermique pendant l'intervention. 
    
    Mes travaux actuels proposent une refonte de ces approches en couplant le mesure expérimentale par IRM avec des modèles physiques thermiques afin d'augmenter la précision des mesures et de fournir au praticien des mesures hybrides à haute résolution spatiale et temporelle pour l'aide à la décision lors de la procédure. 

    Différents dispositifs médicaux mini-invasifs tels que le laser, la radiofréquence ou les micro-ondes, ou des dispositifs non-invasifs comme les ultrasons de haute intensité peuvent être utilisés. Deux thérapies sont principalement concernées: l'oncologie pour le traitement des tumeurs cancéreuses et la cardiologie pour l'ablation des tissus cardiaques arythmogènes responsables des arythmies cardiaques."    

    keywords: ["Temperature Mapping", "Thermo-Ablation", "Image-guided therapy", "Real-time processing", "Medical Devices"]
    links: "/thermoablation/"

  - title: "Thermorégulation, hyperthermie et cartographie thermique par IRM"
    content: "TODO"
    keywords: ["Thermoregulation", "Hyperthermia", "Heatstroke"]
    links: "/hyperthermie/"

  - title: "Etude de l'architecture cardiaque par IRM de diffusion"
    content: "TODO"
    keywords: [ "Architecture cardiaque", "IRM de diffusion" , "Arythmie"]
    links: /microstructure/
---

Je suis chargé de recherche au CNRS, et rattaché au Centre de Résonance Magnétique des Systèmes Biologiques à Bordeaux. 

Mes travaux portent sur le développement de nouvelles méthodes d’imagerie thermique par IRM. Mon cœur de métier concerne le développement d’algorithmes de reconstruction ou de traitements d’images innovants pour transformer le signal brut IRM en information de température interprétable, le tout avec une contrainte de temps réel.

Mots clés:
<div class="keywords">
  {% for skw in page.special_keywords %}
    <span class="kww">{{ skw }}</span>
  {% endfor %}
</div>
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