{% import "macros.jinja" as macros with context %}

Here are a bunch of example scripts, including everything from the rest of the (public) site.

If you don't find an example similar to what you're trying to do, request that it be added (bottom right).
If you figure it out yourself, consider adding your script to the collection!
If you aren't comfortable putting up pre-publication work, Jeff can:

* embargo it until the paper comes out
* partially anonymize it by switching out the genes and genomes involved

<input id="scriptsearch" placeholder="Search example scripts" id="box" type="text"/>

<div id="scripts">
{% for path in examples | sort() %}
  {%- filter markdown -%}
	{%- include "loadexample.html" -%}
  {%- endfilter -%}
	<p></p>
{% endfor %}
</div>
