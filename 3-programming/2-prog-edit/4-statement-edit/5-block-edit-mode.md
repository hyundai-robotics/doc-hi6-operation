# 3.2.4.5 Block Editing Mode

You can set a single line or multiple lines of a program as a block to perform copy, move, delete, and remark operations.
<br>

#### 1. Entering Block Edit Mode

In the job editing panel, move the cursor to the address area using the left arrow key.
Click the `F2: Blk.edit` button to enter block edit mode, and the cursor will turn gray.

![](../../../_assets/tp630/blockedit/11_blockeditmode2.PNG)
![](../../../_assets/tp630/blockedit/12_blockeditmode.PNG)
<br><br>

#### 2. Setting a Block

Use the up/down arrow keys to move the cursor to the starting position of the block and press the `ENTER` key. Then, move the cursor to the end position of the block using the up/down arrow keys and press `ENTER` again. The selected block will be highlighted with a blue background.

![](../../../_assets/tp630/blockedit/20_set_block.PNG)

(If you perform an action like copying or deleting without moving the cursor away from the block, you do not need to press `ENTER` a second time.) 
<br><br>

#### 3. Copy

While the block is selected, click `F2: copy` to copy the content to the clipboard.
Alternatively, you can click `F2: copy` without selecting a block to copy just a single line.
<br><br>

#### 4. Paste

Move the cursor to the line above where you want to paste using the up/down arrow keys, then click `F3: paste`.
For example, if you want to paste the copied block below the `delay 1` statement in S1, place the cursor on `delay 1` and click `F3: paste`.

![](../../../_assets/tp630/blockedit/30_paste.PNG)
![](../../../_assets/tp630/blockedit/32_paste.PNG)
<br><br>

#### 5. Cut

When a block is selected, clicking `F1: cut` will make the block appear in light gray, indicating that it has been cut.  
Alternatively, you can click `F1: cut` without selecting a block to cut a single line.

![](../../../_assets/tp630/blockedit/40_cut.PNG)

Pasting a cut block follows the same method as described above.
<br><br>

#### 6. Delete
When a block is selected, clicking `F4: delete` and then confirming the `Delete?` prompt will remove the block.  
Alternatively, you can click `F4: delete` without selecting a block to delete a single line.

 ![](../../../_assets/tp630/blockedit/50_delete.PNG)
<br><br>

#### 7. Remark, Unremark

This feature is used to temporarily disable the execution of a specific section in a job program without deleting it.  
When a block is selected and you click `F5: remark`, the statements within the block are commented out (remarked).
When a block is selected and you click `F6: unremark`, the comments are removed (unremarked).  
Additionally, you can comment or uncomment a single line without selecting a block.

{% hint style="info" %}
- Less than version V60.30-00 : Steps are not remarked.
- Version V60.30-00 or later : Steps are also remarked.
{% endhint %}

 ![](../../../_assets/tp630/blockedit/60_remark.PNG)
<br><br>


#### 8. Auto Comment / Remove Comments

(This feature is supported from version V70.01-00 and later.)

- Press the `[R5: Prev/next]` button to display the `[F1: auto comment]` and `[F2: uncomment]` buttons.

- When you press `[F1: auto comment]`, the registered data comments are automatically inserted on the selected statements.

  * For how to configure data comments, refer to [4.11 data comment](../../../4-service/11-data-cmts.md).

  * For application conditions, refer to section [4.3.9 Statement data comment](../../../4-service/3-program-conversion/9-stmt-comment.md).

- When you press `[F2: uncomments]`, the comments of the selected statements are removed (regardless of whether data is registered).

![](../../../_assets/tp630/blockedit/66_auto_comment.PNG)


#### 9. Closing Block Edit Mode

Block edit mode can be closed by clicking `F7: close` or pressing the `ESC` key.
<br><br>


----

#### Auto-adjusting Step #

For example, if steps S1-S2 are copied and pasted below, the `move` statement originally at S3 will be pushed down and renumbered as S5 due to the inserted 2 steps.

In this case, all branch statement within the same job such as `goto`, `gosub`, `if` statements, and the timeout address of `wait` statements' target addresses will be automatically adjusted from S3 to S5.

For instance, in the example below, the conditional branch statement `if di45==0 then S3` will be updated to S5 to ensure it still branches to the same `move` statement as before.

![](../../../_assets/tp630/blockedit/71_branch_adjust.PNG)
![](../../../_assets/tp630/blockedit/72_branch_adjust.PNG)

This automatic step number adjustment is performed for operations that shift step numbers forward or backward, such as recording, deletion, and block editing.

{% hint style="info" %}
The following specifications apply from version V60.30-00 and later.
{% endhint %}

If a target step is removed due to deletion or remarking, it will be adjusted as `deleted_step#` or `remarked_step#`, as shown below.  
Please manually adjust these modified target addresses to the appropriate step number (or line number/label).
(If left unchanged, a syntax error will occur when executing the statement.)

![](../../../_assets/tp630/blockedit/76_branch_adjust.PNG)
