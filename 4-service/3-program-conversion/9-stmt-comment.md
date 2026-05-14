# 4.3.9 Statement Comments

(This feature is supported in version V70.02-00 and later.)

This feature automatically attaches comments to statements using pre-configured data comments. It also includes functions to delete comments in bulk or assign serial numbers to `spot` statements (Spot Welding commands).

For details on how to configure data comments, please refer to [4.11 Data Comments](../11-data-cmts.md).

* Execution Example 1: Signal assignment, `wait`, `move` statements

  ![](../../_assets/tp630/prog-conv/prog-conv-data-job1.png)


* Execution Example 2: `spot` statement
  
  ![](../../_assets/tp630/prog-conv/prog-conv-data-job2.png)


### Operation Method

(1) Select `[F1: Service] -> 6: Program conversion -> 9: Statement data comment`.

![](../../_assets/tp630/prog-conv/prog-conv-data-cmt.png)

(2) Configure the settings below, then press the `[F7: OK]` key to run the process.

- `Source Program`

  The number of the original program you wish to apply comments to. If set to 0, the operation will be performed across all ranges of all jobs.

- `Target Program`

  The program number where the results will be saved. If this is the same as the `Source program` number, the file will be overwritten.

- `Start step` ~ `End step`

  The specific range of steps where you want to apply the changes. (Default: 0 ~ last step).
  For example, if set to 2–5, the changes will be applied starting from the move statement at Step 2 through to the final function of Step 5.


- `Existing comment`

  * `Delete all` : Deletes existing comments instead of applying new ones. (This only removes the comments attached to the statement; it does not delete the comment statement lines.)
    
  * `Overwrite` : If a statement already has a comment, it will be replaced with the new one.

  * `Skip` : If a statement already has a comment, that specific statement will be bypassed and left as is.

 
- `Affected commends` (Hidden if `Existing comment` is set to `Delete all`.)

   Select the types of commands to which you want to apply comments.

   * `LHS of assignment`: Uses the comment associated with the variable on the Left-Hand Side of an assignment statement as the statement comment.

   * `move`: For `move` statements containing a `tg=` argument, the comment of the first pose variable in the assigned pose expression is used. (Note: This does not apply to hidden pose `move` statements.)

   * `wait`, `if` (including `elseif`), `switch`: Uses the comment of the variable specified in the conditional parameters as the statement comment.

   * `spot`: Assigns a serial number within the job scope as the statement comment.
   For example, if you set the prefix to `W.P.=` and the starting number to 101, the first spot statement will be commented as `W.P.=101`, the second as `W.P.=102`, and so on.

- `Prefix`
  
  Defines the prefix for the serial numbers applied to `spot` statement comments. You can edit this using the soft keyboard.

- `Starting number`

  Sets the initial number for the serial sequence applied to `spot` statement comments.

----

### Notes

- If the conditional parameter of a statement is an expression, the comment is determined based on the variable occupying the first character of that expression. For example, if `di1` is commented as `part check` and `di2` is `vacuum check`, the following `if` statement will be assigned the comment `part check`:

    ```python
    if di1=0 and di2=0 then 90 # part check
    ```

- In the Block Editing Mode of the job edit screen, you can also automatically insert or remove comments for selected statements. Unlike this screen, the application conditions for this mode are fixed as follows:

  * `Existing comment`: `Overwrite`

  * `Affected commands`: All commands except `spot`

For further details, please refer to [3.2.4.5 Block Editing Mode](../../3-programming/2-prog-edit/4-statement-edit/5-block-edit-mode.md).
 