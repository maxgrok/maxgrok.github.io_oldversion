---
layout: post
title: "YAML _templates"
author: Max
tags: Octopress YAML _templates Update
subtitle: Octopress Update
category: Blog Scaffolding
date: 2017-01-06T14:57:15-05:00
---

### What is YAML? 

YAML originally stood for "Yet Another Markup Language". Now, it stands for "YAML - Ain't Markup Language"[^1]. YAML is "a human friendly data serialization
  standard for all programming languages"[^2]. It is "commonly used for configuration files, but could be used in many applications where data is being stored (e.g. debugging output) or transmitted (e.g. document headers)"[^3]. 

### What is front matter? 

  Front matter is "the first section of a book and is generally the shortest; it is also sometimes called the prelims, or preliminary matter"[^4].

### What is YAML front matter?

  In this case, it is used for document headers for the site or any data that you want to be immediately incorporated into the new page, post, or draft for the static site. Information in the YAML front matter includes the date, layout, title, author, etc. 

  What does it look like? 
  {% highlight ruby %}
---
layout:     post
title:      Octopress
date: 2017-01-05T17:54:20-05:00
---
  {% endhighlight %} 

### What was the YAML front matter problem?

 The problem was that the posts were not formatted properly as the other manually generated posts were. The result of the ```octopress new post "New Post"``` command looked like the following.

 I just resolved the YAML front matter problem that I was experiencing yesterday. Here's how. 

The YAML looked like this:
{% highlight ruby %}
---
layout:     post
title:      Octopress
date: 2017-01-05T17:54:20-05:00
---
{% endhighlight %}

Instead of this: 
{% highlight ruby %}
---
layout:     post
title:      Octopress
author:     Max
tags: 		Update
subtitle:   Blog Scaffolding
category:   Blog Scaffolding
date: 2017-01-05T17:54:20-05:00
published: false
---
{% endhighlight %}

### What's a YAML _template?

It refers to the YAML front matter that is in the ```_templates``` folder. The files within the ```_templates``` folder signify templates for the YAML front matter for Octopress commands. For example, the ```post``` file contains the YAML front matter for the default to posts used in the ```octopress new post "New Post"``` command. The same is true for the draft and page files found by default in the ```_templates``` folder. 

So, I learned that in the _templates folder that there are three files: one for drafts, one for pages, and one for posts. In order to solve my problem, I edited the YAML for the post file. This created a template for the ```octopress new post "New Post"``` command to generate a post with the same YAML front matter as the other posts. 

Now, the YAML looks like this: 
{% highlight ruby %}
---
layout: post
title: "TEST"
author: Max
tags: Update
subtitle: Update
category: Update
date: 2017-01-06T15:06:54-05:00
published: false
---
{% endhighlight %}

I'm excited to have found and fixed the problem this quickly! 

Now, I need the Disqus comments to work. I'll be up and running in no time! 

[^1]:For more information see YAML." YAML - Wiktionary. N.p., n.d. Web. 06 Jan. 2017.
[^2]:For more information see "The Official YAML Web Site." The Official YAML Web Site. N.p., n.d. Web. 06 Jan. 2017. 
[^3]:For more information see "YAML." Wikipedia. Wikimedia Foundation, n.d. Web. 06 Jan. 2017.
[^4]:For more information see Inc, Scribendi. "Front Matter: What It Is and Why It Is Important." Scribendi.com. N.p., n.d. Web. 06 Jan. 2017.

<p style="margin:0 auto;">Works Cited (MLA 7):</p> 
Inc, Scribendi. "Front Matter: What It Is and Why It Is Important." Scribendi.com. N.p., n.d. Web. 06 Jan. 2017.
"The Official YAML Web Site." The Official YAML Web Site. N.p., n.d. Web. 06 Jan. 2017. 
YAML." YAML - Wiktionary. N.p., n.d. Web. 06 Jan. 2017.
"YAML." Wikipedia. Wikimedia Foundation, n.d. Web. 06 Jan. 2017.
