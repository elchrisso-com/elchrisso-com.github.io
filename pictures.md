---
title: Pictures
layout: default
---

# Pictures

<style>
.image-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center; /* Center the entire gallery */
}

.image-item {
  width: 400px;
  display: flex;
  align-items: center;
  justify-content: center; /* Center each image within its container */
  text-align: center; /* Center text or captions if added */
}

.image-item img {
  width: 100%;
  height: auto;
  border-radius: 5px;
}
</style>

<div class="image-gallery">
  {% for image in site.static_files %}
    {% if image.path contains 'img/' %}
      <div class="image-item">
        <img src="{{ image.path | relative_url }}" alt="{{ image.name }}" />
      </div>
    {% endif %}
  {% endfor %}
</div>

