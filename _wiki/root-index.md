---
layout  : wikiindex
title   : wiki
toc     : true
public  : true
comment : false
updated : 2023-03-15 19:47:26 +0900
regenerate: true
---

## [[how-to]]

* [[mathjax-latex]]

* 여기에 글을 작성하면 [[이제부터]]!

---

## blog posts
<div>
    <ul>
{% for post in site.posts %}
    {% if post.public == true %}
        <li>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                {{ post.title }}
            </a>
        </li>
    {% endif %}
{% endfor %}
    </ul>
</div>

