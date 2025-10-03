## 关于本项目

 Telegram自动开会员源代码 基于 `Golang` ，这是一个完整的24小时全自动开通TG会员的代码，如果你会一点技术，可无缝对接至你的机器人实现24小时自动代开。

## 开始
~~这只是一个demo版本，没有写配置文件，使用之前，你应该详细阅读源代码里的备注，修改应该代码里备注需要修改的地方。~~  
请仔细查看`.env`配置文件的说明,如配置错误导致付款以后会员未开通，自行负责。

**如不会获取配置文件的 `COOKIE` 与 `Hash` 请进交流群自行询问，或动手能力强的自行研究。**

### 安装环境
项目运行基于`Golang`，你需要先安装`Golang`

+ Windows
  > https://go.dev/ 前往Golang官方网站进行下载安装，如不会建议Google。
+ Linux
   - Centos  
  > yum install golang
  - Ubuntu  
  > sudo apt-get install golang

### 安装依赖

+ golang  
    >   go mod init   
        go mod tidy   
        或者  
        go install

### 运行OR编译
+ Windows
  > 直接运行  
    go run main.go  
    编译运行  
    go build .
+ Linux
  > 同上，如需在windows下交叉编译Linux 请自行 `golang 交叉编译`


## 实现逻辑

1. 通过解析https://fragment.com的数据
2. 指定开通会员的用户名
3. 解析出相关Payload
4. 携带Payload进行Ton支付
5. 支付完成，开通完成。

