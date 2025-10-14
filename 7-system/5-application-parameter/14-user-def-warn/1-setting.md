# 7.5.14.1 User-Defined Warning Settings

1. Touch the \[System &gt; 4: Application Parameters &gt; 14: User-Defined Warning\] menu.<br><br>

2. Click the 'Create Sample File' button.<br>
* A file named 'help_user_warn.json' will be created in the MAIN/project directory.<br>
![](../../../_assets/tp630/user-def-code/image5.png)

3. When re-entering the settings screen, the user-defined warnings written in the sample file will be displayed.
- Warning Code: Specifies the warning code to be triggered.
- Condition Expression: Defines the condition for triggering the warning. Any condition expression that can be used in an if statement is allowed.
- Message: Specifies the message displayed when the warning occurs.<br>
![](../../../_assets/tp630/user-def-code/image6.png)

4. Insert a USB drive into the teaching pendant, access the File Manager menu, and copy the 'help_user_warn.json' file to the USB storage path.<br><br>
![](../../../_assets/tp630/user-def-code/image7.png)

5. Open the file on a PC and edit the warnings according to the sample file format (editing with Notepad is possible).<br><br>
- W65###: Warning Code (Range: W65001 ~ W65100)
    - cnd: Condition expression
    - msg: Cause message displayed in the warning help
    - remedy: Corrective action displayed in the warning help<br>
![](../../../_assets/tp630/user-def-code/image8.png)

6. Copy the edited file back to the teaching pendant.