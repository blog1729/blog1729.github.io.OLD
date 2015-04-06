---
layout: post
title: What's Jekyll?
comments: True
---

[Jekyll](http://jekyllrb.com) is a static site generator, an open-source tool for creating simple yet powerful websites of all shapes and sizes. From [the project's readme](https://github.com/mojombo/jekyll/blob/master/README.markdown):

  > Jekyll is a simple, blog aware, static site generator. It takes a template directory [...] and spits out a complete, static website suitable for serving with Apache or your favorite web server. This is also the engine behind GitHub Pages, which you can use to host your project’s page or blog right here from GitHub.

It's an immensely useful tool and one we encourage you to use here with Hyde.

Find out more by [visiting the project on GitHub](https://github.com/mojombo/jekyll).

* * *

**This blog supports Kramdown (a superset of Markdown)**

## Examples

### Code


{% highlight cpp linenos %}
#include<iostream>
#include<string>
int main()
{
	std::cout<<"What is your name?";
	std::string name;
	std::cin>>name;
	std::cout<<"Hello"<<name<<std::endl;
	return 0;
}
{% endhighlight %}

### Math

$$\int\limits_{0}^{\pi} \sin x \,\text{d}x > 0 $$ 
