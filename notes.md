# Web Dev

## HTML
Important points:
* There are two kinds of tags in HTML:
	* *block* tags takes up complete block of row in html documents.
	* *inline* tags takes as width as its content is and doesn't spawn on new line.

* There are some tags that are deprecated but still works because of legacy reasons. e.g. center tag

* Add video
```html
<video controls>
	<source src="">
</video>
```
* add tables
```html
<style>
        table, td, th {
            border: 1px solid black;
        }
<table>
	<thead>
		<tr>
			<th>col 1</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td colspan=2>col 1 value</td>
			<td>col 3 value</td>
		</tr>
		<tr>
			<td>col 1 value</td>
			<td rowspan="2">Col 2 Value</td>
			<td>col 3 value</td>
		</tr>
		<tr>
			<td>col 1 value</td>
			<td>col 3 value</td>
		</tr>
	</tbody>
</table>
```

* forms - forms allow us to take inputs from the user.


