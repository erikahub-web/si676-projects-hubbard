<!-- display an unordered list of the shopping list data -->
<ul>
{% for item in test-jekyll-site.data.shopping-list %}
  <li><strong>{{ item.name }}</strong> has type {{ item.type }}</li>
{% endfor %}
</ul>

<!-- display a table of the shopping list data -->
<table>
    <thead><th>Name</th><th>Type</th></thead>
    <tbody>
        {% for item in test-jekyll-site.data.shopping-list %}
        <tr>
            <td>{{ item.name }}</td>
            <td>{% if item.type %}{{ item.type }}{% endif %}</td>
        </tr>
        {% endfor %}
    </tbody>
</table>