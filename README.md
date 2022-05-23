# KRENEL-REBUILD
伺服器建設
* [KERNEL-REBUILD 前置作業](#kernel-rebuild-前置作業)


## KERNEL-REBUILD 前置作業
### 設定記憶體大小
- 由於REBUILD的檔案相當大,經反覆測試後50GB為最佳的記憶體大小

### 確認目前內核版本
- 若是下載的kernel比目前所使用的版本還舊的話,即使安裝完畢,系統仍會顯示舊的kernel,例如在UBUNTU20.4(內核為5.13.40)上安裝內核5.9.6,最後顯示的仍是5.13.40

- 為避免上述的問題,會需要用到uname –mrs進行確認



