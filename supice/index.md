---
layout: default
rbar: 
   - fb
   - calendar


#{% include homepage/banner.html 
#   link='/komunalni-volby/'
#   title='Komunální volby 2018'
#   default='banner-default.jpg'
#   mobile='banner-mobile.jpg'
#   breakpoint=640
#%}
---
<div class="row">
  <div class="medium-12 large-8 columns">
    <section class="o-section o-section--spaceBot">
      <div class="o-section-inner o-section-inner--leftBlock">
        <header class="o-section-header">
          <h1 class="o-section__heading">Aktuální témata</h1>
        </header>
        {% for article in site.posts limit: 6 %}
          {% include articles/horizontal-article.html article=article %}
        {% endfor %}
        <div class="c-article-listing__nextbox">
          <a href="{{'/aktuality/' | relative_url}}" rel="next" class="button expanded large">Další články</a>
        </div>
      </div>
    </section>
  </div>
  {% if page.rbar %}
  <div class="medium-12 large-4 columns">
    {% include right-bar/rbar.html param='rbar' %}
  </div>
  {% endif %}
</div>