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

## CSS

* CSS tag Based selector
* changing block element, `display: block/inline`

### Layouts
**Flexbox**
```html
.flex-layout {
    display:flex;
    flex-direction: column;
}

.flex-layout div {
    background: red;
    width: 200px;
    height: 200px;
    margin: 10px;
    border: 2px solid black;
}
```

**flexbox basis**
There are two axis the **main** axis which is the row to which the boxes are being added and the **cross axis** which is perpendicular to the main axis.

```css
.flex-layout {
    display:flex;
    flex-direction: row;
}

.flex-layout div {
    background: red;
		flex-basis: 300px; 
		/* It becomes width in row and height in column 
			flex-basis points to the length of the selected item in the flex-direction.
			flex-basis only works in the direction of the main axis.
		*/
    width: 200px;
    height: 200px;
    margin: 10px;
    border: 2px solid black;
}
```

**Main axis is the axis in which the items are being added.**

**flex-shrink**
It is basically a propotion of compared to other elements how much a particular element should shrink to fit. 0 means not to shrink at all.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="/sytle.css">
</head>
<body>
    <nav>
        <ul>
            <li>Home</li>
            <li>About</li>
        </ul>
    </nav>
    <section>
        <div id="logo"></div>
    </section>
    <footer>
        <div class="layer">Footer 1</div>
        <div class="layer">Footer 2</div>
    </footer>
</body>
</html>
```

```css
.flex-layout {
    display:flex;
    flex-direction: row;
}

.first {
    flex-shrink: 1;
}

.second {
    flex-shrink: 2
}
.flex-layout div {
    background: red;
    flex-basis: 200px;
    height: 200px;
    margin: 10px;
    border: 2px solid black;
}
```

**flex-wrap**
This property overflows the element to the next row if it does not fit in the previous row.
```css
.flex-layout {
    display:flex;
    flex-direction: row;
    flex-wrap: wrap;
}

.flex-layout div {
    background: red;
    flex-basis: 200px;
    height: 200px;
    margin: 10px;
    border: 2px solid black;
}
```

**Center a div**
```css
* {
    margin: 0;
}
#parent {
    background: red;
    width: 100vw;
    height: 100vh;
    display: flex; 
    justify-content: center;  /* flex-start, flex-end */
    align-items: center; /* flex-start, flex-end */
}

#child {
    background: yellow;
    width: 200px;
    height: 200px;
    margin: 5px;
}
```

**flex-grow**
flex-grow means take as much as space it could take. `flex-grow: 1;`

**Example**
```css
* {
    margin: 0;
}

body {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

nav, footer {
    flex-shrink: 0;
}

section {
    flex-grow: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

nav ul {
    display: flex;
    justify-content: flex-end;
}

nav ul li {
    list-style-type: none;
    padding: 20px;
    margin: 10px;
}

#logo {
    width: 80vw;
    height: 200px;
    background: red;
}

.layer {
    background: grey;
    padding: 20px 10px;
}
```

### Position

* all elements comes with a property of position static.
* `position: absolute` takes body as parent if no parent with `position: relative` is passed.
* `position: fixed` fixes the element to the body.
* `position: sticky; top: 0px`
 