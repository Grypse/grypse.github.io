---
layout: post
title:  "Welcome to Jekyll!"
brief:  "Introduce the basic concept of Jekyll"
date:   2015-08-18 10:12:38
image:  "/images/n33-robot-invader.jpg"
categories: jekyll
---
#What is Jekyll, exactly?
Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free.

#Quick-start guide
For the impatient, here’s how to get a boilerplate Jekyll site up and running.
{% highlight ruby linenos %}
  ~ $ gem install jekyll
  ~ $ jekyll new myblog
  ~ $ cd myblog
  ~/myblog $ jekyll serve
  # => Now browse to http://localhost:4000
{% endhighlight %}

If you wish to install jekyll into the current directory, you can do so by alternatively running jekyll new . instead of a new directory name.

That’s nothing, though. The real magic happens when you start creating blog posts, using the front matter to control templates and layouts, and taking advantage of all the awesome configuration options Jekyll makes available.

If you’re running into problems, ensure you have all the requirements installed.

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
