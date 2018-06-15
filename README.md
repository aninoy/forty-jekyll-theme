# Personal Website

This website was made using the Forty - Jekyll Theme, a Jekyll version of the "Forty" theme by [HTML5 UP](https://html5up.net/).

# How to Use

* For those unfamiliar with how Jekyll works, check out [jekyllrb.com](https://jekyllrb.com/) for all the details,
* or read up on just the basics of [front matter](https://jekyllrb.com/docs/frontmatter/), [writing posts](https://jekyllrb.com/docs/posts/), and [creating pages](https://jekyllrb.com/docs/pages/).
* To insert gists use this shortcode: `{% gist sha-code %}`
* To highlight code use this format:
```
	{% highlight python %}
	  # your code
	{% endhighlight %}

```
* Uses MathJax with Kramdown for Mathemetical Equations in LaTeX using this format:
```
	{% raw %}
	  $$J(w, b) = 1/m \sum_{i=1}^{m}L(\hat{y}^{(i)}, y^{(i)})$$
	  $$= 1/m \sum_{i=1}^{m} y^{(i)}\log \hat{y}^{(i)} + (1-y^{(i)})\log (1 - \hat{y}^{(i)})$$
	{% endraw %}
```
* Run locally with `bundle exec jekyll serve`

# Added Features

* **[Formspree.io](https://formspree.io/) contact form integration** - just add your email to the `_config.yml` and it works!
* Use `_config.yml` to **set whether the homepage tiles should pull pages or posts**, as well as how many to display.
* Add your **social profiles** easily in `_config.yml`. Only social profiles buttons you enter in `config.yml` show up on the site footer!
* Set **featured images** in front matter.

