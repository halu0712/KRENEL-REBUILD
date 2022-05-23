# KRENEL-REBUILD
伺服器建設
* [KERNEL-REBUILD 前置作業](#kernel-rebuild-前置作業)
    - [設定記憶體大小](#設定記憶體大小)
    - [確認目前內核版](#確認目前內核版)
    - [安裝GUESS ADDITIONS CD 映像](#安裝GUESS ADDITIONS CD 映像)
       - [步驟一](#步驟一)


## KERNEL-REBUILD 前置作業
### 設定記憶體大小
- 由於REBUILD的檔案相當大,經反覆測試後50GB為最佳的記憶體大小

### 確認目前內核版本
- 若是下載的kernel比目前所使用的版本還舊的話,即使安裝完畢,系統仍會顯示舊的kernel,例如在UBUNTU20.4(內核為5.13.40)上安裝內核5.9.6,最後顯示的仍是5.13.0-41

- 為避免上述的問題,會需要用到uname –mrs進行確認

     ![uname-mrs](image/uname-mrs.png) 

### 安裝GUESS ADDITIONS CD 映像
由於基礎視窗過小,所以如果是有需要進行Mesunconfig的需求的話會無法執行,故需要利用GAC來使視窗大小改變

#### 步驟一
在介面上方找到"裝置",點擊他並找到"插入GAC映像"
    
![install-GAC](image/install-GAC.png)

點選後會跑出以下圖示,點"執行"後系統會自行跳出終端並安裝,結束後按ENTER即跳出視窗

![GAC-confirm](image/GAC-confirm.png)

#### 步驟二
結束之後打開終端,並執行以下指令

```shell
sudo apt-get apdate
```

```shell
sudo apt-get apgrade
```

```shell
sudo apt-get install dkms
```
上述動作結束後重開機,並在上方欄位"檢視"中找到選項"自動調整客體顯示大小",即可調節視窗大小
