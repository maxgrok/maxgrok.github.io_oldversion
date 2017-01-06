---
layout: post
title: "Octopress: YAML _templates"
author: Max
tags: Update
subtitle: Update
category: Blog Scaffolding
date: 2017-01-06T14:57:15-05:00
---

I just resolved the YAML front matter problem that I was experiencing yesterday. The problem was that the posts were not formatted properly as the other manually generated posts were. 

For instance, YAML looked like this:
{% highlight ruby %}
layout:     post
title:      Octopress
date: 2017-01-05T17:54:20-05:00
{% endhighlight %}

Instead of this: 
{% highlight ruby %}
layout:     post
title:      Octopress
author:     Max
tags: 		Update
subtitle:   Blog Scaffolding
category:   Blog Scaffolding
date: 2017-01-05T17:54:20-05:00
{% endhighlight %}

So, I learned that in the _templates folder that there are three files: one for drafts, one for pages, and one for posts. I edited the YAML for the post file. This created a template for the ```octopress new post "New Post"``` command to generate a post with the same YAML front matter as the other posts. 

I'm excited to have found and fixed the problem this quickly! 

Now, I need to tackle the Disqus comments to work. 