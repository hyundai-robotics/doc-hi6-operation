# 7.5.13.1 User-Defined Error Settings

1. Touch the `[System  - 4: Application Parameters  - 13: User-Defined Error]` menu.<br><br>

2. Click the "Create Sample File" button.<br>
A file named "help_user_err.json" will be created in the MAIN/project directory.<br>
![](../../../_assets/tp630/user-def-code/image1.png)

3. When re-entering the settings screen, the user-defined errors written in the sample file will be displayed.<br>
- Error Code: Specifies the error code to be triggered.
- Condition Expression: Defines the condition for triggering the error. Any condition expression that can be used in an - if statement is allowed.
- Message: Specifies the message displayed when the error occurs.
- Motor Off: Determines whether the motor should turn off when a user-defined error occurs.<br>
![](../../../_assets/tp630/user-def-code/image2.png)

4. Insert a USB drive into the teaching pendant, access the File Manager menu, and copy the 'help_user_err.json' file to the USB storage path.<br><br>
![](../../../_assets/tp630/user-def-code/image3.png)

5. Open the file on a PC and edit the errors according to the sample file format (editing with Notepad is possible).<br><br>
- E65###: Error Code (Range: E65001 ~ E65500)
    - cnd: Condition expression
    - msg: Cause message displayed in the error help
    - remedy: Corrective action displayed in the error help
    - mot_off: Motor off<br>
![](../../../_assets/tp630/user-def-code/image4.png)

6. Copy the edited file back to the teaching pendant.

