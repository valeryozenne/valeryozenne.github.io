---
layout: index
keywords: [MRI, Temperature Mapping, Thermo-Ablation, Real-time]
---

Je suis chargé de recherche au CNRS, et rattaché au Centre de Résonance Magnétique des Systèmes Biologiques à Bordeaux. 

Mes travaux portent sur le développement de nouvelles méthodes d’imagerie thermique par IRM, pour permettre de suivre en temps réel le déroulement de procédures interventionnelles. Ces procédures visent à détruire des tissus pathologiques via un dépôt d’énergie localisé. Mon cœur de métier concerne le développement d’algorithmes de reconstruction ou de traitements d’images innovants pour transformer le signal brut IRM en information de température interprétable, le tout avec une contrainte de temps réel.

<!--
I’m a researcher in medical imaging in a [CNRS](https://www.cnrs.fr/fr/page-daccueil) laboratory, the "Centre de Résonance Magnétique des Systèmes Biologiques" (Bordeaux, France).
-->

Mots clés: Imagerie par résonance magnétique, Mesure de temperature non invasive, Thermoablation, Dispositifs Médicaux.

## Imagerie interventionnelle et cartographie thermique par IRM

Différents dispositifs médicaux mini-invasifs tels que le laser, la radiofréquence ou les micro-ondes, ou des dispositifs non-invasifs comme les ultrasons de haute intensité peuvent être utilisés. Deux thérapies sont principalement concernées: l'oncologie pour le traitement des tumeurs cancéreuses et la cardiologie pour l'ablation des tissus cardiaques arythmogènes responsables des arythmies cardiaques.

## Thermoregulation et cartographie thermique par IRM

## Etude de l'architecture cardiaque par IRM de diffusion

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
