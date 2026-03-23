# 6.3.3.3 变量文件

变量值也会以文件形式保存，因为即使在关机时也必须保留它们，而全局变量根据类型以两种形式存储：

<table>
  <thead>
    <tr>
      <th style="text-align:left">类型</th>
      <th style="text-align:left">路径</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        全局根数组变量
      </td>
      <td style="text-align:left">MAIN/project/vars/*.csv</td>
      <td style="text-align:left">为每个变量创建一个文件，文件标题与变量名称相同。</td>
    </tr>
	 <tr>
      <td style="text-align:left">
        其他变量
      </td>
      <td style="text-align:left">MAIN/project/vars/vars.json</td>
      <td style="text-align:left">所有其他全局变量作为一个文件保存。</td>
    </tr>
	</tbody>
</table>

<br>


##### vars/.csv 文件

当您在文件管理器中打开文件夹 `MAIN/project/vars/` 时，将创建一个名为 `weld_points.csv` 的文件。指定为预定义的变量创建一个与变量名称相同的 .csv 文件，当从预定义中释放时，该文件会被自动删除。

![](../../../_assets/tp630/panel-gvar/csv0.png)

通过 USB 存储器或 FTP 复制此文件，并在您的 PC 上打开它。 .csv 文件是一种非常简单的文本格式标准，表示以逗号分隔的值。

参考： [维基百科：逗号分隔值](https://en.wikipedia.org/wiki/Comma-separated_values)

该 .csv 文件表示一个单一的二维表。列通过逗号分隔，行通过换行符分隔。

![](../../../_assets/tp630/panel-gvar/csv1.png)

csv 文件按顺序包含构建 `weld_points` 二维数组的过程。

对于每一行，第一列是索引，第二列是类型，第三至最后一列是值。第一行将其描述为表的标题。

第二行是创建顶层的行，即 `weld_points` 本身。因此，索引列为空，类型为数组，数字为 10。换句话说，创建了 weld_points[10]，并用零填充了 10 个元素。

```python
, , array, 10
```

以下行生成并分配姿态类型值给 `weld_points[0]` 的元素。

```python
[0][0][0], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[0][0][1], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

如果对 `weld_points[0]` 执行 100 行，以下行将跟随 `weld_points[1]` 的操作，如下所示：

```python
[1][1], array; 100
[1][1][0], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][1], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][2], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

您可以在文件管理器中双击 .csv 文件以使用 Microsoft Excel 打开并进行编辑。编辑完成时按 `Ctrl+S` 或 `保存 (Save)` 按钮保存。

![](../../../_assets/tp630/panel-gvar/csv2.png)

在 Excel 中保存会导致不必要的逗号，如下所示，坐标系中的引号消失，导致格式略有变化。这是因为 Excel 以这样的方式处理 .csv。无论如何，${cont_model} 控制器也能够识别这种格式，因此没关系。

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

##### 加载 .csv

您可以将编辑后的文件覆盖到 `MAIN/project/vars/` 中，但它不会自动反映到内存中。

当您在全局变量窗口中单击 [F2: load all] 按钮时，`vars/` 文件夹中的所有变量文件将重新加载到内存中。
(请注意，删除变量文件并单击 [F2: load all] 也会删除内存中对应的变量。)

![](../../../_assets/tp630/panel-gvar/fixed-var.png)