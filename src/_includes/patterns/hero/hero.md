
<section class="usa-hero"{% if hero.image %} style="background-image: url({{ hero.image }})"{% endif %} aria-label="Introduction">
  <div class="grid-container">
    <div class="usa-hero__callout">
      {% if hero.callout %}<h1 class="usa-hero__heading">
      {% if hero.callout.alt %}<span class="usa-hero__heading--alt">{{ hero.callout.alt }}</span>{% endif %}
      {{ hero.callout.text | default: hero.callout }}
      </h1>
      {% endif %}
      {{ hero.content | markdownify }}
      {% if hero.button %}<div><a class="usa-button"
        href="{{ hero.button.href }}">{{ hero.button.text }}
      </a></div>{% endif %}
      </div>
    </div>

  </div>
</section>