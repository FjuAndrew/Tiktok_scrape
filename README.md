"# Tiktok_scrape" 

"利用DrissionPage這個python套件，進行Tiktok簡單的數據爬蟲"

基本上有幾個常用的方法  
=====  

一開始啟動瀏覽器  
page = ChromiumPage() #也可在()裡加上想要指定的port  
page.get('輸入要查詢的Tiktok頻道主頁')


定位元素常用的方法  
-----

page.ele('')  
找class用.  
找id用#  
其他元素可用@+元素名稱  
例如:要找name='123'的元素  
可用以下程式碼  
page.ele('@name=123')   
如果要找多個同名稱元素則用  
page.eles('') 元素查找的方式都一樣  


Function介紹
-------

* get_basic_info()
裡面含有三個元素查找 分別是用來查詢
![Tiktok](https://github.com/user-attachments/assets/0f80a13c-ffc5-4706-a3ab-81159494215a)  
最後有一個print()可以方便查看爬取到的數據

* ge_content()
用來抓取頻道主頁下方的影片標題及對應的觀看次數
是以同元素名稱做抓取，因此使用page.eles()  
定位元素後做DataFrame的轉換  
接著print出來

最後是主程式的執行順序
* 首先try訪客登入 #如果有跳出登入畫面的話會以訪客繼續登入 如果沒有出現的話 則會往下一步前進
* get_basic_info()首先抓取頻道的概覽資料
* get_content()最後抓取頻道主頁裡出現的影片標題以及觀看次數

