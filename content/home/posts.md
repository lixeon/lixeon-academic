---
# An instance of the Pages widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: pages

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 60

title: Recent Posts
subtitle: 最近的博客随笔

content:
  # Page type to display. E.g. post, talk, publication...
  page_type: post
  # Choose how many pages you would like to display (0 = all pages)
  count: 6
  # Filter on criteria
  filters:
    author: ""
    category: ""
    tag: ""
    exclude_featured: false
    exclude_future: false
    exclude_past: false
    publication_type: ""
  # Choose how many pages you would like to offset by
  offset: 0
  # Page order: descending (desc) or ascending (asc) date.
  order: desc

design:
  # Choose a view for the listings:
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   4 = Citation (publication only)
  view: 1
  
design.background:
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.
  
  # Background color.
  # color = "navy"
  
  # Background gradient.
  gradient_start: "#FFFFF8"
  gradient_end: "#BBCCEE"
  
  # Background image.
  # image = "home.jpg"  # Name of image in `static/media/`.
  image_darken: 0.0  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
  image_size: "cover"  #  Options are `cover` (default), `contain`, or `actual` size.
  image_position: "center"  # Options include `left`, `center` (default), or `right`.
  image_parallax: true  # Use a fun parallax-like fixed background effect? true/false

  # Text color (true=light or false=dark).
  # text_color_light = true  
---
