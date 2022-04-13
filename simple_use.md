## 開始建置我們的環境
在 laradock/ 資料夾裡面執行
$ cp .env-example .env

## 建立好 .env 之後，我們來開啟運行網站所需的服務
$ docker-compose up -d nginx mysql workspace

這邊的參數不能省略！省略了會一次打開所有的服務，電腦會撐不住！

