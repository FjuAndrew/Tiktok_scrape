"# Tiktok_scrape" 

"利用DrissionPage這個python套件，進行Tiktok簡單的數據爬蟲"

基本上有幾個常用的方法

一開始啟動瀏覽器
page = ChromiumPage() #也可在()裡加上想要指定的port

定位元素常用的方法
page.ele('')
找class用.
找id用#
其他元素可用@+元素名稱
例如:要找name='123'的元素
可用以下程式碼
page.ele('@name=123')
如果要找多個同名稱元素則用
page.eles('') 元素查找的方式都一樣
