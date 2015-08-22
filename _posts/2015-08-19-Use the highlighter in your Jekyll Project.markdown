---
layout: post
title:  "Use the highlighter for your Jekyll Project"
date:   2015-08-19 16:01:01
image:  "/images/4547.png"
brief:  Introduce how to use the highlighter in your jekyll project
categories: jekyll
---
#Code snippet highlighting
Jekyll has built in support for syntax highlighting of over 100 languages thanks to Pygments. To use Pygments, you must have Python installed on your system and set highlighter to pygments in your site's configuration file.

Alternatively, you can use Rouge to highlight your code snippets. It doesn’t support as many languages as Pygments, however it should suit most use cases. Also, since Rouge is written in pure Ruby, you don’t need Python on your system!

To render a code block with syntax highlighting, surround your code as follows:
{% highlight html %}
{ % highlight ruby % }
def foo
  puts 'foo'
end
{ % endhighlight % }
{% endhighlight %}

And the output will look like this:
{% highlight ruby %}
def foo
  puts 'foo'
end
{% endhighlight %}

The argument to the highlight tag (ruby in the example above) is the language identifier. To find the appropriate identifier to use for the language you want to highlight, look for the “short name” on the [Pygments’ Lexers page][Lexers] or the [Rouge wiki][rouge].

#Line numbers
There is a second argument to highlight called lineos that is optional. Including the lineos argument will force the highlighted code to include line numbers. For instance, the following code block would include line numbers next to each line:

{% highlight html %}
{ % highlight ruby linenos % }
def foo
  puts 'foo'
end
{ % endhighlight % }
{% endhighlight %}

And the output will look like this:

{% highlight ruby linenos %}
def foo
  puts 'foo'
end
{% endhighlight %}
#Stylesheet for syntax highlighting
In order for the highlighting to show up, you'll need to include a highlighting stylesheet. For an example stylesheet you can look at [syntax.css][syntax].Except, you can find it in this article's end .These are the same stylesheet as used by Github and you're free to use them for your own site. If you use __lineos__, you might want to include an addtional CSS class defination for the **.lineos** class in **syntax.css** to distinguish the line numbers from the highlighted code.

{% highlight css %}
.highlight  { background: #ffffff; }
.highlight .c { color: #999988; font-style: italic } /* Comment */
.highlight .err { color: #a61717; background-color: #e3d2d2 } /* Error */
.highlight .k { font-weight: bold } /* Keyword */
.highlight .o { font-weight: bold } /* Operator */
.highlight .cm { color: #999988; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #999999; font-weight: bold } /* Comment.Preproc */
.highlight .c1 { color: #999988; font-style: italic } /* Comment.Single */
.highlight .cs { color: #999999; font-weight: bold; font-style: italic } /* Comment.Special */
.highlight .gd { color: #000000; background-color: #ffdddd } /* Generic.Deleted */
.highlight .gd .x { color: #000000; background-color: #ffaaaa } /* Generic.Deleted.Specific */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #aa0000 } /* Generic.Error */
.highlight .gh { color: #999999 } /* Generic.Heading */
.highlight .gi { color: #000000; background-color: #ddffdd } /* Generic.Inserted */
.highlight .gi .x { color: #000000; background-color: #aaffaa } /* Generic.Inserted.Specific */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #555555 } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #aaaaaa } /* Generic.Subheading */
.highlight .gt { color: #aa0000 } /* Generic.Traceback */
.highlight .kc { font-weight: bold } /* Keyword.Constant */
.highlight .kd { font-weight: bold } /* Keyword.Declaration */
.highlight .kp { font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #445588; font-weight: bold } /* Keyword.Type */
.highlight .m { color: #009999 } /* Literal.Number */
.highlight .s { color: #d14 } /* Literal.String */
.highlight .na { color: #008080 } /* Name.Attribute */
.highlight .nb { color: #0086B3 } /* Name.Builtin */
.highlight .nc { color: #445588; font-weight: bold } /* Name.Class */
.highlight .no { color: #008080 } /* Name.Constant */
.highlight .ni { color: #800080 } /* Name.Entity */
.highlight .ne { color: #990000; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #990000; font-weight: bold } /* Name.Function */
.highlight .nn { color: #555555 } /* Name.Namespace */
.highlight .nt { color: #000080 } /* Name.Tag */
.highlight .nv { color: #008080 } /* Name.Variable */
.highlight .ow { font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mf { color: #009999 } /* Literal.Number.Float */
.highlight .mh { color: #009999 } /* Literal.Number.Hex */
.highlight .mi { color: #009999 } /* Literal.Number.Integer */
.highlight .mo { color: #009999 } /* Literal.Number.Oct */
.highlight .sb { color: #d14 } /* Literal.String.Backtick */
.highlight .sc { color: #d14 } /* Literal.String.Char */
.highlight .sd { color: #d14 } /* Literal.String.Doc */
.highlight .s2 { color: #d14 } /* Literal.String.Double */
.highlight .se { color: #d14 } /* Literal.String.Escape */
.highlight .sh { color: #d14 } /* Literal.String.Heredoc */
.highlight .si { color: #d14 } /* Literal.String.Interpol */
.highlight .sx { color: #d14 } /* Literal.String.Other */
.highlight .sr { color: #009926 } /* Literal.String.Regex */
.highlight .s1 { color: #d14 } /* Literal.String.Single */
.highlight .ss { color: #990073 } /* Literal.String.Symbol */
.highlight .bp { color: #999999 } /* Name.Builtin.Pseudo */
.highlight .vc { color: #008080 } /* Name.Variable.Class */
.highlight .vg { color: #008080 } /* Name.Variable.Global */
.highlight .vi { color: #008080 } /* Name.Variable.Instance */
.highlight .il { color: #009999 } /* Literal.Number.Integer.Long */
{% endhighlight %}
[Lexers]:http://pygments.org/docs/lexers/
[rouge]:https://github.com/jayferd/rouge/wiki/List-of-supported-languages-and-lexers
[syntax]:https://github.com/mojombo/tpw/tree/master/css/syntax.css
