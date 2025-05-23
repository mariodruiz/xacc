# Publications

This page lists the research publications which have been carried out in the context of the HACC program, or papers that may be of interest to the HACC community.

## Contribute

If you would like to contribute to this page by adding a reference to your publication, please follow the [contribution guidelines](contributing.md).

<!--
DO NOT MODIFY THIS FILE.

TO ADD YOUR PAPER, PLEASE EDIT THE YAML FILE IN docs/_data/publications/<year of publication>.yaml
-->

{% assign years = "2025,2024,2023,2022,2021,2020,2019,2018,2017,2016" | split: "," %}

Search publication by year:

{% for year in years %}[{{ year }}](#{{ year }}){% unless forloop.last %}, {% endunless %}{% endfor %}

{% for year in years %}

## {{ year }}

<table width="100%">
    <tr>
        <th width="320">Title & Abstract</th>
        <th width="100">Author(s)</th>
        <th width="100">Institution</th>
        <th width="40">Link</th>
    </tr>

    {% for item in site.data.publications[year] %}
    <tr>
        <td>
            {{ item.title }} <br>
            <details>
                <summary>Abstract</summary>
                {{ item.abstract }}
            </details>
            {% if item.bestpaper %}
                <img src="./images/best_paper_award.png" alt="Best Paper" height="100">
            {% endif %}
        </td>
        <td>{{ item.author }} <em>et al.</em></td>
        <td>{{ item.institution }}</td>
        <td>
            <a href="{{ item.link }}">Paper</a>
            {% if item.github %}
                <br><a href="{{ item.github }}">GitHub</a>
            {% endif %}
        </td>
    </tr>
    {% endfor %}
</table>

{% endfor %}

---------------------------------------
<p class="copyright">Copyright&copy; 2022-2025 Advanced Micro Devices</p>
