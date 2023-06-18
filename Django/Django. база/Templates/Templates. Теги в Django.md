синтаксис {% _тег_ %}, часто имеет закрывающий тег в конце {% /_тег_ %}

< ul>
	{% for athlete in athlete_list %}
		< li>{{ athlete.name }}< /li>
	{% endfor %}
< /ul>

Доступны к использованию те же операторы сравнения, что и в питоне
{% if athlete_list _and_ coach_list %}
	Both athletes and coaches are available.
{% endif %}

{% if _not_ athlete_list %}
	There are no athletes.
{% endif %}

{% if athlete_list _or_ coach_list %}
	There are some athletes or some coaches.
{% endif %}

{% if not athlete_list _or_ coach_list %}
	There are no athletes or there are some coaches.
{% endif %}

{% if athlete_list _and_ _not_ coach_list %}
	There are some athletes and absolutely no coaches.
{% endif %}

{% if somevar == "x" %}
	This appears if variable somevar equals the string "x"
{% endif %}

{% if somevar != "x" %}
{% endif %}

{% if somevar < 100 %}
{% endif %}

_forloop.counter_ The current iteration of the loop (1-indexed)
_forloop.counter0_ The current iteration of the loop (0-indexed)
_forloop.revcounter_ The number of iterations from the end of the loop (1-indexed)
_forloop.revcounter0_ The number of iterations from the end of the loop (0-indexed)
_forloop.first_ True if this is the first time through the loop
_forloop.last_ True if this is the last time through the loop
_forloop.parentloop_ For nested loops, this is the loop surrounding the current one

for . . . empty
The for tag can take an optional {% empty %} clause whose text is displayed if the given array is empty or
could not be found:
< ul>
	{% for athlete in athlete_list %}
		< li>{{ athlete.name }}</li>
	{% empty %}
		< li>Sorry, no athletes in this list.</li>
	{% endfor %}
</ ul>