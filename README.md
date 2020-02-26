# single-file-guis

Can a single file construct and manage a GUI?

```
sql categories	select * from categories		
sql boards	select * from boards		
sql threads	select * from threads		
sql posts	select * from posts where thread_id = ?		
			
			
page index	"<table>
{% for category in categories %}
<tr>
{{ category.name }}
</tr>
{% for board in category.boards %}
<tr><a href=""boards/{{ board.id }}"">{{ board.name}}</a></tr>
{% endfor %}
{% endfor %}
</table>
"		
			
			
			
page thread list	"<table>
{% for thread in threads %}
<tr>
<a href=""{{thread.id }}"">{{ thread.title }}</a>
</tr>
{% endfor %}
</table>
"		
			
page posts list	"<table>
{% for post in posts %}
<tr>
{{ post.body }}
</tr>
{% endfor %}
</table>
"	edit page	"<table>
<textarea>{{ post.body }}</textarea>
</table>
"

```
