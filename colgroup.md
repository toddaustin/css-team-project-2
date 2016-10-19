#&lt;colgroup&gt;
---
* the &lt;colgroup&gt; is used for formatting one or more columns within a table.

Just like we use `<thead>`, `<tbody>`, `<tfooter>` to group header, body and footers respectively, we could group columns using the html `<colgroup>` tag.

## Syntax

 `<colgroup>` may not have an end tag but good a good practise to specify it as:
 `<colgroup span=1 />`.

`<colgroup>` child may be `<col>` to specify grouping of columns.
`<colgroup>` must be child of `<table>`, after `<caption>`(if present) and before `<thead>`, `<tbody>`, `<tfoot>`, `<tr>`

## Description
Generally, creation of table can happen using the below format using `<tr>` and `<td>`.
* 
```
<table>
<!-- Header Row -->
<tr>
<th>First Header</th>
<th>Second Header</th>
</tr>
<!-- Row Data -->
<tr>
<td> r1c1</td>
<td>r1c2</td>
</tr>
<tr>
<td> r2c1</td>
<td>r2c2</td>
</tr>
</table>

```
As seen in the code snippet, table creation starts with a table row. `<colgroup>` enables us to do logical grouping of columns of the table.

What would this enable us to do?
This tag provides us with a cool feature to set color, width or possibly any property that applies to the cell on a column level.

Eg: Color the first column of the table to blue.
```
<table>
<colgroup style="background-color:blue" span="1"/>
<!-- Header Row -->
<tr>
<th>First Header</th>
<th>Second Header</th>
</tr>
<!-- Row Data -->
<tr>
<td> r1c1</td>
<td>r1c2</td>
</tr>
<tr>
<td> r2c1</td>
<td>r2c2</td>
</tr>
</table>

```

## Attribute
Most of the attributes that apply to a cell also applies to `<colgroup>` element but are deprecated in HTML5.
* align
* char
* charoff
* span
* valign
* width