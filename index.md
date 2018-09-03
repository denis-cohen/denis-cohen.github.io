---
layout: home
---

<p style="text-align:justify">
 <img alt="Denis Cohen" src="assets/images/logo5.1.png"
 style="float:right;margin:5px 0px 10px
 30px;width:260px">
 I am a Postdoctoral Fellow in the <a
 href="https://www.mzes.uni-mannheim.de/d7/en/dm-unit">Data and Methods Unit</a> at the <a
 href="https://www.mzes.uni-mannheim.de/d7/en">Mannheim Centre for European Social Research (MZES)</a>, <a
 href="https://www.uni-mannheim.de/en/">University of Mannheim</a>. <br>  <br>
 My research focus lies at the intersection of political preference formation, electoral behavior
 and political competition.
 My methodological interests include quantitative approaches to the
 analysis of clustered data, measurement models, data visualization, strategies for causal
 identification and Bayesian statistics. <br> <br>
 I hold a BA in Social Sciences from
 <a href="https://www.hu-berlin.de/">Humboldt-University Berlin</a> (2013) and an MSc in Political Economy
 from the <a href="http://essex.ac.uk/">University of Essex</a> (2014).
 Prior to joining the <a
 href="https://www.mzes.uni-mannheim.de/d7/en">MZES</a>, I finished my PhD at the <a href="https://www.bgss.hu-berlin.de/de/bgss/">Berlin Graduate School
 of Social Sciences</a> at <a href="https://www.hu-berlin.de/">Humboldt University of Berlin</a>, where I also worked as a research associate in the <a href="https://www.sowi.hu-berlin.de/en/lehrbereiche-en/comppol-en">Comparative Politics Unit</a>.</p>
 <br/>


<h2 id="news">News</h2>

<section class="archive">
{% for post in site.posts %}
{% unless post.next %}

  {% unless forloop.first %}
    </div>
  </div>
  {% endunless %}

  <div class="archive-item fadeInDown animated">
    <h2>{{ post.date | date: '%Y' }}</h2>
    <div>

{% else %}

{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
{% capture next_year %}{{ post.next.date | date: '%Y' }}{% endcapture %}

{% if year != next_year %}

  {% unless forloop.first %}
    </div>
  </div>
  {% endunless %}

  <div class="archive-item fadeInDown animated">
    <h2>{{ post.date | date: '%Y' }}</h2>
    <div>

{% endif %}
{% endunless %}

  <article>
    <a href="{{ post.url | absolute_url }}" title="{{ post.title }}">{{ post.title }}</a>
    <div class="post-date">
      <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%-d %B" }}</time>
    </div>
  </article>

  {% if forloop.last %}
    </div>
  </div>
  {% endif %}

{% endfor %}
</section>
