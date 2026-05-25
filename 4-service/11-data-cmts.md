<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi6", "Hi7"]
}
</script>

# 4.11 Data Comments

(This feature is supported from version V70.02-00 and later.)

You can register comments for IO variables, relays of the built-in PLC, and other general variables. The registered comments are displayed as tooltips in the monitoring panels. (`public input`, `public output`, `fn input`, `fn output`, `global variable`, `memory variable`, `watch` monitoring)

Additionally, using the features below, the registered comments can be automatically attached onto each statement of the job program.

* [4.3.9 Statement data comment](3-program-conversion/9-stmt-comment.md)
* [3.2.4.5 Block Editing Mode](../3-programming/2-prog-edit/4-statement-edit/5-block-edit-mode.md) - `[auto comment]` button.

The comments configured on this screen are saved to the `project/DataCmt.txt` file in the main module.

![](../_assets/tp630/data-cmt/data-cmt.png)


### Data Comments Screen

   1. Select `[F1: Service] - 4: Data comment` to open the screen.

   2. Use the filter combo boxes at the top to select the desired data category and type.

   3. The selected data will be displayed in a table. You can view the name, comment, and current value of each item.

   4. For `fb.dio`, `fn.dio`, and `relay` objects, all indices are displayed. Indices with registered comments will show the comments, while those without will have an empty comment field.

   5. `etc` displays only items (excluding IO and relays) among various global variables that have registered comments. (Do not register comments for local variables, as their meaning may vary depending on the sub-job.) The data type is displayed according to the variable type.


### Navigation

   1. You can move between items by pressing the `Up`/`Down` arrow keys. Press them while holding the `Ctrl` key to move faster.

   2. Alternatively, you can jump directly to a specific index by entering the number in the `Name` column. (Note: This is not available for `etc` objects.)

   3. A maximum of 1,000 items can be displayed at once. For types with a larger maximum index (such as `M`-Relays), you cannot view them all on one screen. You must navigate through pages using the method described in above 2.


### Edit, Save, and Load

   1. You can enter or edit comments in the `Comment` column using the numeric keypad or the soft keyboard.

   2. To remove an existing comment, simply delete the text in the comment column. (Empty strings are treated as unregistered.)

   3. Pressing `[F7: OK]` or `[SHIFT]+[F7: Apply]` will apply your edits to the main module and save them to the `DataCmt.txt` file.

   4. Pressing `[F1: Clear]` will delete all items. (Changes will only be reflected in the file after pressing `[F7: OK]`.)

   5. Pressing `[F2: Reload]` reloads the `DataCmt.txt` file and refreshes the data comment screen on the TP.

   6. Pressing `[F3: Sort]` will not change the current screen display, but the data will be saved in a sorted state when you press `[F7: OK]`. If you save without sorting, the original order in the file will be preserved.

   7. The Value column cannot be edited.


### `DataCmt.txt` File

   1. Alternatively, you can edit the `DataCmt.txt` file directly on a PC using a text editor. The image below shows an example of the file opened in `Visual Studio Code`.

      ![](../_assets/tp630/data-cmt/data-cmt-file.png)

   2. The file is in `tsv (Tab-Separated Values)` format. Each row consists of a Name and Comment pair. The Name and Comment must be separated by at least one tab character.

   3. The file format is compatible with the `Import Relay Description` / `Export Relay Description` functions in HRLadder. Therefore, the created file can be used interchangeably between Hi6/Hi7 controllers and HRLadder. (It is also compatible with Hi5a controllers; however, differences in relay or variable names may require adjustment.)

   4. For I/O or relay names, the system recognizes both the Built-in PLC style (UPPERCASE) and the hrscript style (lowercase) as identical. (For example, `FB5.DIB3` and `fb5.dib3` are treated as the same.) For variables, however, the case must match exactly.

   5. If comments contain non-English characters, the file encoding must be saved as UTF8-BOM. (If only English comments are used, both ANSI and UTF8-BOM are acceptable.)
