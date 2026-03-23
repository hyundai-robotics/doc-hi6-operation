# 7.5.14.1 用户定义警告设置

1. 触摸`[System - 4: Application Parameters - 14: User-Defined Warning] ([System  - 4: Application Parameters  - 14: User-Defined Warning])`菜单。<br><br>

2. 点击“创建示例文件”按钮。<br>
* 将在MAIN/project目录中创建一个名为'help_user_warn.json'的文件。<br>
![](../../../_assets/tp630/user-def-code/image5.png)

3. 重新进入设置屏幕时，将显示在示例文件中写入的用户定义警告。
- 警告代码：指定要触发的警告代码。
- 条件表达式：定义触发警告的条件。可以使用if语句中的任何条件表达式。
- 消息：指定在发生警告时显示的消息。<br>
![](../../../_assets/tp630/user-def-code/image6.png)

4. 将USB驱动器插入教学挂件，访问文件管理器菜单，并将'help_user_warn.json'文件复制到USB存储路径。<br><br>
![](../../../_assets/tp630/user-def-code/image7.png)

5. 在PC上打开文件并根据示例文件格式编辑警告（可以使用记事本进行编辑）。<br><br>
- W65###: 警告代码（范围：W65001 ~ W65100）
    - cnd: 条件表达式
    - msg: 在警告帮助中显示的原因消息
    - remedy: 在警告帮助中显示的纠正措施<br>
![](../../../_assets/tp630/user-def-code/image8.png)

6. 将编辑后的文件复制回教学挂件。