## 安裝
git clone https://github.com/Laradock/laradock.git
## 開始建置我們的環境
在 laradock/ 資料夾裡面執行
```
$ cp .env-example .env
```
## 建立好 .env 之後，我們來開啟運行網站所需的服務
$ docker-compose up -d nginx mysql workspace

這邊的參數不能省略！省略了會一次打開所有的服務，電腦會撐不住！

注意：所有的 Web 服務器容器..etc 都依賴於nginx，這意味著如果您運行其中任何一個，它們將自動為您啟動容器，因此無需在命令中明確指定它。
如果必須這樣做，您可能需要按如下方式運行它們：.apachephp-fpmphp-fpmupdocker-compose up -d nginx php-fpm mysql

您可以從此列表中選擇您自己的容器組合。

### Sample
這個例子中，我們將看到如何運行 NGINX（Web 服務器）和 MySQL（數據庫引擎）來託管 PHP Web 腳本：
```
docker-compose up -d nginx mysql

# 查詢 port
netstat -ant | grep 8080

```

