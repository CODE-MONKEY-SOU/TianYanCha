### 天眼查项目爬虫
#### 作者信息
* 姓名：周家宏
* 博客：JoeZJH.github.io
* 时间：2020年1月24日

#### 用途说明
* 女朋友需要从天眼查上爬取公司的注册地址，本项目用于帮助女朋友节约时间

#### 输入文件（注意格式和Sheet名称必须相同才能解析）
company_list.xlsx

#### 输出文件 
company_info.xls

#### 用法说明
##### 环境配置
* python3.6环境
* pip 命令安装以下包
    * beautifulsoup4
    * requests
    * xlrd
    * urllib
    * xlwt
##### 使用步骤
* 将需要爬取的文件打包成xlsx格式，Sheet名称为"Sheet2"，文件命名为company_list.xlsx
* 将文件放到当前目录下
* 修改crawler.py文件中的`target_headers`对象中的`Cookie`属性为自己浏览器的（需要先从浏览器手动登陆天眼查网站）
* 运行crawler.py文件
```
python crawler.py
```

#### 附件说明
* 如果想拓展爬取公司的其他信息可修改解析函数
* 如果不想命名为"Sheet2"，请修改程序中的`sheet_name`为对应的名称即可