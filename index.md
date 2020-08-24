## My Coordinates

Fred Zimmerman  
2846 S. Knightsbridge Cir.  
Ann Arbor, MI 48105-9288  
fredzannarbor@gmail.com 

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
