---
layout: page
title: Page 1
permalink: Page1.html
description: Description
---
<html>

{% include head.html %}

<body>

    {% include header.html %}

    <!-- Main -->
    <article id="main">
        <header{% if page.image %} style="background-image: url('{% if site.featured-image-source %}{{ page.image | prepend: site.featured-image-source | absolute_url }}{% else %}{{ "" | absolute_url }}/assets/images/{{ page.image }}{% endif %}');"{% endif %}>
            <h2>{{ page.title }}</h2>
        </header>
        <section class="wrapper style5">
            <div class="inner">

                {{ content }}

            </div>
        </section>
    </article>

    {% include footer.html %}

</body>

</html>
