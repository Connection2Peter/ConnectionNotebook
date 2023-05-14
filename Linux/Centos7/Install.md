Centos USB 安裝流程
===

事前準備
---

1. 材料
    1. 下載 Centos 7 安裝 ISO 檔
        - [Centos 官方網站](https://www.centos.org/)
        - [陽明交通大學站點](http://centos.cs.nctu.edu.tw/)
    2. 一個 USB，最小大小如下 :
        - Minimal     : 至少  4 GB
        - DVD         : 至少  8 GB
        - Everything  : 至少 16 GB 
    3. 一台要安裝的伺服器
    4. Rufus 應用程式
        - 用途為把 ISO 檔燒錄成開機 USB
        - [Rufus 官網](https://rufus.ie/)

開機 USB 建立
---

1. 開啟 Rufus
2. 設定
    - 裝置 : 選擇要安裝的 USB
    - 開機模式 : 選擇要安裝的 ISO 檔案
3. 點選 **執行**
4. 開機 USB　建立完成

Bios 設定
---

1. 確保電腦是關機的，然後插上開機的 USB
2. 開機並進入主機板 Bios
    - 每張主機板開啟 Bios 方式都不同，查詢方法 :
        1. 開機過程中會出現按某些按鍵可以進入 Bios setting
        2. 上網查
3. Bios 需要調整的設定
    1. (重要) 開機順序
        - 把 USB 安裝碟拉到第一順位
    2. (可選) 效能設定
        - 關閉自動效能調節，強制鎖在最高效能
        - 關閉風扇調節，強制使用最高散熱
4. 儲存 Bios 設定
5. 重新啟動

Centos 7 基本安裝
---

1. 正常重開後來說會看到這個畫面，選取 Install CentOS 7
    ![image](https://github.com/Connection2Peter/ConnectionNotebook/assets/69660530/760d21aa-6a81-42a1-841f-99269b6e4819)
2. 選擇語言
3. 設定日期時間到指定時區
4. 設定需要的語言支援
5. 設定軟體選擇
6. 安裝目的地
    1. 選取主系統硬碟
    2. 選擇硬碟分割
        - 自動分割
        - 手動分割
7. 網路與主機名稱的設定
    - 建議先設定完成，因為進去再用指令改很麻煩
8. 開始安裝
9. 設定 Root 密碼
10. 建立第一位用戶
11. 安裝完成後會要求重新起動，直接按下去
12. (重要) 再次進入 Bios 把 USB 開機順序調到後面，或是在關機以及開機過程中手動移除
13. 系統安裝成功
