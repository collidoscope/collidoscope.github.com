{% include header.html %}
<body class="{{ page.layout }}">
  <div id="outer">
{% include logo.html %}
{% include navigation.html %}
{{ content }}
{% include disqus.html %}
{% include footer.html %}
{% include tail.html %}