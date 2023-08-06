# 6.3.3.3 Variable files

Variable values are also saved as files because they must be preserved even when powered off, and global variables are stored in two forms, depending on the type:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Pathname</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        Global root array variables
      </td>
      <td style="text-align:left">MAIN/project/vars/*.csv</td>
      <td style="text-align:left">One file is created for each variable, and the file title is the same as the variable name.</td>
    </tr>
	 <tr>
      <td style="text-align:left">
        Other variables
      </td>
      <td style="text-align:left">MAIN/project/vars/vars.json</td>
      <td style="text-align:left">All other global variables are saved as a single file.</td>
    </tr>
	</tbody>
</table>

<br>


## vars/.csv file

When you open the folder `MAIN/project/vars/` in File-manager, a file named `weld_points.csv` is created. The variables specified as the predefined create a .csv file that is the same as the variable name, and when released from predefined, the file is automatically deleted.

![](../../_assets/tp630/panel-gvar/csv0.png)

Copy this file via USB memory or FTP and open it on your PC. The .csv file is a very simple text format standard that expresses comma-separated values.

Refer to: [Wikipedia: Comma-separated values](https://en.wikipedia.org/wiki/Comma-separated_values)

The .csv file represents a single two-dimensional table. The columns are separated by commas and rows are spearated by line-feed.

![](../../_assets/tp630/panel-gvar/csv1.png)

The csv file containing the procedure building up the `weld_points` two-dimensional array, in order.

For each row, the 1st column is the index, the 2nd column is the type, and the 3rd ~ last columns are the values. The 1st row describes this as the header of the table.

The 2nd row is the row that creates the top level, that is, `weld_points` itself. Therefore, the index column is empty, type is array, and number is 10. In other words, weld_points[10] is created, and 10 elements are filled with the default value of zeroes.

```python
, , array, 10
```

The following rows generate and assign pose type values to the elements of `weld_points[0]`.

```python
[0][0][0], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[0][0][1], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

If 100 rows are performed for `weld_points[0]`, the following rows are followed by the action for `weld_points[1]` as shown below:

```python
[1][1], array; 100
[1][1][0], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][1], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][2], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

You can double-click the .csv file in File-manager to open it with Microsoft Excel and edit it. Save as `Ctrl+S` or `Save` button when editing is done.

![](../../_assets/tp630/panel-gvar/csv2.png)

Saving in Excel results in unnecessary commas, as shown below, and the quotation marks in the coordinate-system disappear, resulting in a slight change in format. It can't be helped because Excel handles .csv like this. Anyway, the Hi6 controller also recognizes that kind of format, so it doesn't matter.

```python
, , array,10,,,,,,
[0][0], array,100,,,,,,
[0][0][0], Pose,0,90,10,0,20,0,
[0][0][1], Pose,0,0,0,0,0,0,base
[0][0][2], Pose,0,10,0,0,0,0,robot
[0][0][3], Pose,0,20,0,0,0,0,base
[0][0][4], Pose,0,0,0,0,0,0,base
[0][0][5], Pose,0,0,0,0,0,0,base
```

<br>

## Loading .csv

You can overwrite the edited file into `MAIN/project/vars/` again, but it is not automatically reflected in memory.

When you click the [F2: load all] button in the Global Variables window, all variable files in the `vars/` folder are reloaded to memory.
(Please note that deleting the variable file and clicking [F2: load all] will also delete the corresponding variable in memory.)

![](../../_assets/tp630/panel-gvar/fixed-var.png)
