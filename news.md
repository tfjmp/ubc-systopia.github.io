---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
# To add a heading image, upload the img to /assets and type the file name + extension into "headerimg"

layout: page
headerimg: 
tagline: Updates and Accomplishments
heading: News
description: Read more about our recent activities--including papers, posters, talks, and internships.
---
<!-- .recent_papers_posters -->
<div class="container">
    <div class="row mb-5">
        <div class="col">
            <h4 class="mb-4">Recent Papers and Posters</h4>
            {% for publication in site.data.recent-papers-posters %}
            <p><B><a href="{{ publication.link}}">{{ publication.title }}.</a></B> {{ publication.authors }}. {{ publication.publisher }}.
                {% if publication.info %}
            <ul><li>{{ publication.info }}</li></ul>
                {% endif %}
            </p>{% endfor %}
        </div>
    </div>
</div>
<!-- /.recent_papers_posters -->
<!-- .recent_talks -->
<div class="container">
    <div class="row mb-5">
        <div class="col">
            <h4 class="mb-4">Recent Talks</h4>
            {% for talk in site.data.recent-talks %}
            <ul>
                <li>
                    <B>{{ talk.speaker }}</B>: {{ talk.title }}, <a href="{{ talk.link}}">{{ talk.event }}.</a> 
                        {% if talk.video-link %}
                    <a href="{{ talk.video-link }}">[Video]</a>
                        {% endif %}
                </li>
            </ul>
            {% endfor %}
        </div>
    </div>
</div>
<!-- /.recent_talks -->
<!-- .internships -->
<div class="container">
    <div class="row mb-5">
        <div class="col">
            <h4 class="mb-4">Internships</h4>
            {% for internship_date in site.data.internships %}
                <h5 class="mb-4">{{ internship_date.date }}</h5>
                    {% for internship in internship_date.internship %}
                        <ul class="mb-4">
                            <li><B>{{ internship.intern }}</B>: <a href="{{ internship.org-link}}">{{ internship.organization }}</a></li>
                        </ul>
                    {% endfor %}
            {% endfor %}
        </div>
    </div>
</div>
<!-- /.internships -->