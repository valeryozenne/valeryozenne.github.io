---
layout: page
---

[# Reproducible Science is good. Replicated Science is better.]::

<!---
# Bla Bla
-->

I’m a researcher in medical imaging at [CNRS](https://www.cnrs.fr/fr/page-daccueil) and the Centre de Résonance Magnétique des Systèmes Biologiques (Bordeaux, France).

Mes travaux portent sur le développement de nouvelles méthodes d’imagerie, permettant de suivre en temps réel le bon déroulement de procédures interventionnelles (ou intervention médicale) sous IRM. 

Je m'intéresse particulièrement au suivi de procédures de thermoablation. Ces procédures visent à détruire des tissus pathologiques via un dépot énergie localisé. Différents dispositifs médicaux mini-invasifs tel que le laser, la radiofréquence ou les micro-ondes ou des dispositifs non-invasifs comme les ultrasons de haute intensité peuvent être utilisés. 

Deux thérapies sont principalement concernées: l'oncologie pour le traitement des tumeurs cancéreuses et la cardialogie pour l'ablation des tissus cardiaques arrythmogènes responsables des arrythmies cardiaques. 

Keywords: Magnetic Resonance Imaging, Thermometry, Thermo-Ablation, Real-time processing, Medical device.

<!---
ReScience C is collaborative and open by design. Everything can be forked and
modified. Don't hesitate to [write a submission](write), [join us](faq) and
to [become a reviewer](https://valeryozenne.github.io/board/).
-->



# Latest articles

{% bibliography --max 4 --sort %}


# Seletected articles

{% bibliography --query @*[pages=116236] %}
{% bibliography --query @*[volume=77]  %}


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


