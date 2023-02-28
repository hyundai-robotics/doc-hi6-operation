# 6.8.2 Predefined-variable feature

If you need to manage a fixed large amount of poses or shift data by editing it in a separate text file, it is efficient to create an predefined-variable.

## Making a predefined-variable

Let's take an example of a 100x100 global two-dimensional array poses named `weld_points`.

Select `weld_points` and click the [F3: Predefined] button. If you select `toggle predef` from the pop-up menu, the type is changed from `array` to `pd.array` (predef.array).

![](../../_assets/tp630/panel-gvar/predef0.png)

If you select `toggle predef` once more, `pd.array` will be restored to `array` again.


{% hint style="warning" %}
\[Warning\] Be aware that defining an array that is too large may take longer to save or load and may fail to save automatically in the event of a power failure.
{% endhint %}

<br>

## Characteristics of an predefined-variable

Predefined-variables have the following differences and constraints compared to general global variables;

1) Saved as a .csv file in the folder `MAIN/project/vars/predef/`. It is an intuitive format that is easy to edit with a text editor.
2) You can only make an array of global variables a predefined-variable. Primitive-types such as int and string or object-types cannot be made into predefined variables. Local variables are also impossible.
3) You can make a variable a predefined only in the Global Variables panel U/I. There are no robot language statements that make the variable a predefined.
4) You cannot assign another value to an predefined-variable. When `weld_points` is a predef. 2-dimensional array;

    - global weld_points : ignored.
    - global weld_points=0 : 'Cannot assign' error occurred
    - weld_points=0 : 'Cannot assign' error occurred
    - weld_points[2]=Array[30]: New value can be assigned to an element.
    - weld_points[2][1]="light": New value can be assigned to an element.
    - weld_points[2][1].j2=90.5: New value can be assigned to an element.


<br>

## predef/.csv file

When you open the folder `MAIN/project/vars/predef/` in File-manager, a file named `weld_points.csv` is created. The variables specified as the predefined create a .csv file that is the same as the variable name, and when released from predefined, the file is automatically deleted.

![](../../_assets/tp630/panel-gvar/predef1.png)

Copy this file via USB memory or FTP and open it on your PC. The .csv file is a very simple text format standard that expresses comma-separated values.

Refer to: https://en.wikipedia.org/wiki/Comma-separated_values

The .csv file represents a single two-dimensional table. The columns are separated by commas and rows are spearated by line-feed.

![](../../_assets/tp630/panel-gvar/predef2.png)

The csv file containing the procedure building up the `weld_points` two-dimensional array, in order.

For each row, the 1st column is the index, the 2nd column is the type, and the 3rd ~ last columns are the values. The 1st row describes this as the header of the table.

The 2nd row is the row that creates the top level, that is, `weld_points` itself. Therefore, the index column is empty, type is array, and number is 100. In other words, weld_points[100] is created, and 100 elements are filled with the default value of zeroes.

```python
, , array, 100
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

![](../../_assets/tp630/panel-gvar/predef3.png)

Saving in Excel results in unnecessary commas, as shown below, and the quotation marks in the coordinate-system disappear, resulting in a slight change in format. It can't be helped because Excel handles .csv like this. Anyway, the Hi6 controller also recognizes that kind of format, so it doesn't matter.

```python
, , array,100,,,,,,
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

You can overwrite the edited file into `MAIN/project/vars/predef/` again, but it is not automatically reflected in memory.

Click the [F3: predef] button in the Global Variables panel. If you select `load from predef/` from the pop-up menu, all files in the `predef/` folder will be reloaded into memory.
(Variables with .csv files become predefined variables, and variables without .csv files are released from default variables.)

![](../../_assets/tp630/panel-gvar/predef0.png)
