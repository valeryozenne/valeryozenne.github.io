---
layout: page
---

[# Reproducible Science is good. Replicated Science is better.]::

<!---
# Bla Bla
-->

I’m a researcher in medical imaging at [CNRS](https://www.cnrs.fr/fr/page-daccueil) and the Centre de Résonance Magnétique des Systèmes Biologiques (Bordeaux, France).

Mes travaux portee sur le développement de nouvelles méthodes d’imagerie, permettant de suivre en temps-réel la destruction des tissus pathologiques lors de procédures interventionnelles sous IRM. Je m'intéresse particulièrement aux procédures de thermoablation qui consiste à délivrer localement de l'énergie via des dispositifs médicaux mini-invasifs (laser, radiofréquence, micro-onde) ou non-invasive (ultrason de haute intensité).

Keywords: Magnetic Resonance Imaging, Thermometry, Thermo-Ablation, Real-time processing, Medical device.

<!---
ReScience C is collaborative and open by design. Everything can be forked and
modified. Don't hesitate to [write a submission](write), [join us](faq) and
to [become a reviewer](https://valeryozenne.github.io/board/).
-->



# Latest articles

{% bibliography --max 3 --sort %}


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


