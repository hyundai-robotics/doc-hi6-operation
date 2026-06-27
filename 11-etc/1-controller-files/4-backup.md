# 11.1.4 backup/

此文件夹存储控制器的MAIN侧备份。  
文件夹名称以格式`bYYYYMMDD_HHMM`生成，包含子文件夹：project/, log/, cifX/, EC_LOG/, 和 EDR_LOG/。


#### backup/ev/

存储事件备份的文件夹。  
当发生特定错误时，备份会自动创建。


#### backup/ts/

存储定期备份的文件夹。  
备份会在预定时间自动创建。