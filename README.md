# AdiDoks Fork for shrs

This is a fork of the Zola [AdiDoks](https://github.com/aaranxu/adidoks) theme used for the shrs website. This README will cover the changes made for this fork specifically. You can check [Zola documentation](https://www.getzola.org/documentation/getting-started/overview/) separately.

## Documentation

### Table of Contents

* [Authors List](#authors-list)
* [Image Styles](#image-styles)

### Authors List

A list of authors can be given in the frontmatter metadata of each blog post. The names do not appear on the post summaries, but they do appear in the title section of each blog. The list consists of two parts: The name and an associated link. Note that the link is an optional parameter. If a link is provided, then the name appears as a hyperlink. An example is given below:

```yaml
title: "First Post"
url: "example.com/first-post"
# ... other frontmatter parameters ...
extra:
  auhtors:
    - name: John Doe
      href: "https://johnswebsite.com"
    - name: Jane Doe

```

The associated macros are in `page-publish-metadata.html` and can be used in template files.

### Image Styles

Images can be added to blog posts using the standard markdown syntax. For blog posts, the styling can be specified in `page.html`. Currently, the only styling applied will limit the width of the image to that of the blogs container.

```html
{% block body %}
  {% set page_class = "blog single" %}
  <style>
    img {
      max-width: 100%;
    }
  </style>
{% endblock body %}```
