# Grid
## A CSS Mobile First Flexbox Grid System

v. 2.7.1

Based on Flexbox (CSS Flexible Box Layout Module), Grid is a very simple css grid system to quickly create modern layouts and submodules.

The concept is simple: you need to wrap your `.col` in a `.grid`.

### What can we expect?
- Each column is the same width as every other cell in the grid.
- But you can add sizing classes to individual columns.
- For responsive designs, you can add classes based on media-queries.
- Media-queries are based on a mobile first approach
- Top, bottom, or middle. For the grid. And for the columns.
- Grids can be nested. Always. Directly in a column.

**I want to include it in my source files!**

Just include gridlex/src/gridlex.scss 
and 
update the $grid- vars:
<table>
    <thead>
    <tr>
        <th>Variable names</th>
        <th>Default value</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td><code>$grid-colCount:</code></td>
        <td><code>12</code></td>
    </tr>
    <tr>
        <td><code>$grid-gridName:</code></td>
        <td><code>grid</code></td>
    </tr>
    <tr>
        <td><code>$grid-colName:</code></td>
        <td><code>col</code></td>
    </tr>
    <tr>
        <td><code>$grid-attributeName:</code></td>
        <td><code>class</code></td>
    </tr>
    <tr>
        <td><code>$grid-gutter:</code></td>
        <td><code>1rem</code></td>
    </tr>
    <tr>
        <td><code>$grid-gutter-vertical:</code></td>
        <td><code>1rem</code></td>
    </tr>
    <tr>
        <td><code>$grid-mq-list:</code></td>
        <td><pre><code>(
         xl: 80em, // 1280px and up
         lg: 64em, // 1024px and up
         md: 48em, // 768px and up
         sm: 36em // 576px and up
	 xs: 20em // 320px and up
 )</code></pre></td>
    </tr>
    </tbody>
</table>

### Install via Npm
**TODO**

### Install via Bower
**TODO**


### 3 ways to use Grid
**1- The basic. Just add a class `.grid-*` (from -1 to -12)**
```html
<div class="grid-1">
	<div class="col">...</div>
</div>
```

**2- The precise. Compose cell by cell (with class like `.col-*`)**
```html
<div class="grid">
	<div class="col-12">...</div>
</div>
```

**3- The automatic. Just add number of cells you want in the grid (`.grid > .col`)**
```html
<div class="grid">
		<div class="col">...</div>
		<div class="col">...</div>
</div>
```

### Gridl and media-queries
Because the web is now responsive, you sometimes need to change the width of columns: with this keys as classes you can control your layout by media-queries.

Columns can be hidden at breakpoints using `_*-0` (e.g. `col-4_md-6_sm-0`)
<table>
<thead>
	<tr>
		<th>CSS Media Query</th>
		<th>Applies</th>
		<th>Usage</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td><code>@media screen and (min-width: 20rem)</code></td>
		<td>320px and up</td>
		<td><code><b>_xs</b>-*</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (min-width: 36rem)</code></td>
		<td>576px and up</td>
		<td><code><b>_sm</b>-*</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (min-width: 48em)</code></td>
		<td>768px and up</td>
		<td><code><b>_md</b>-*</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (min-width: 64em)</code></td>
		<td>1024px and up</td>
		<td><code><b>_lg</b>-*</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (min-width: 80em)</code></td>
		<td>1280px and up</td>
		<td><code><b>_xl</b>-*</code></td>
	</tr>
</tbody>
</table>
