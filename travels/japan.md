---
layout: page
title: RFGeeks
subtitle: A place about engineering, flying, travels, radios and just life.

bigimg:
  - "/img/banner/lilu_bench.jpg" : "Lilu sleeping on the workbench"
  - "/img/banner/flying_FF.jpg" : "Flying near Fergus Falls, MN"
  - "/img/banner/rpi_adsb.jpg" : "Raspberry Pi ADS-B Receiver"
  - "/img/banner/howehall_ant.jpg" : "Antennas on Howe Hall"
  - "/img/banner/bigben.JPG" : "Big Ben - London, UK"
  - "/img/banner/howehall_winter.JPG" : "Howe Hall - Ames, IA"
  - "/img/banner/cy_space.JPG" : "Cy at 70,000 feet"
  - "/img/banner/reiman.jpg" : "Reiman Gardens - Ames, IA"
  - "/img/banner/flying_az.JPG" : "Flying to Sedona, AZ"
  - "/img/banner/elcaptain.JPG" : "El Capitan - Yosemite National Park"
  - "/img/banner/abc_computer.jpg" : "ISU ABC Computer at Computer History Museum"
  - "/img/banner/japan_lego.jpg" : "Nano Blocks - Japan"
  - "/img/banner/bvi.jpg" : "British Virgin Islands"
  - "/img/banner/virgin_island.jpg" : "U.S. Virgin Islands"
  - "/img/banner/piper.jpg" : "Piper PA-28-180 flying near Jefferson, IA"
  - "/img/banner/boston.jpg" : "Boston, MA"
  - "/img/banner/cancun.JPG" : "Cancun, Mexico"
  - "/img/banner/madison.JPG" : "Covered Bridge - Madison County IA"
  - "/img/banner/bunratty.jpg" : "Bunratty, Ireland"
  - "/img/banner/japan_lantern.jpg" : "Kyoto, Japan"
  - "/img/banner/nova_scotia.jpg" : "Peggy's Cover, Nova Scotia"
  - "/img/banner/habet.jpg" : "High Altitude Balloon Launch"

---

<div class="posts-list">
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h2 class="post-title">{{ post.title }}</h2>
	
	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}  
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>
  
    <div class="post-entry">
      {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
	  <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
    </div>
  
   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}