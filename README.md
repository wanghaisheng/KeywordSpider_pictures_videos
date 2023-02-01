## 2023.2.1
### 1.环境配置
* python3.9
* pip install -r requirements.txt
* 如果安装requirements报错，可以按照报错提示安装

### 2.基本设置
* settings.py文件中可以对存储路径、爬取页数、是否下载视频等进行设置

### 3.关键词设置
* 在'全部记录.xlsx'的表格'sheet2'中设置关键词组合，可以直接参照样例设置
* 每行第一格为关键词组合的名称（字典key），每行的其余格为当前组合每次爬取使用的关键词（字典value）
* 程序每次运行需要指定爬取的行，程序会对该行的每个格依次进行爬取，每个格中可以设置多个关键词，用空格分隔

### 4.爬取说明
* 对于涉及鼠标滚轮滑动翻页的任务，程序运行时电脑不能处理其他事务，因为需要模拟鼠标滚轮滑动，鼠标必须位于selenium打开的网页之中
* 对于微信公众号，可以在settings.py中设置快代理的隧道代理IP服务，默认为空，若不设置在爬取量较大时可能会被封IP
* 视频下载可以在settings.py中设置，请慎重选择，受网速限制可能很慢
* 可以下载bilibili与Youtube视频，抖音视频下载请使用其他项目如<https://github.com/JoeanAmier/TikTokDownloader>，快手视频无法下载

### 5.结果说明
* '全部记录.xlsx'的表格'sheet1'中记录爬取到的每条结果的详细信息
* '全部记录.xlsx'的表格'sheet3'中对所有爬取结果中出现的tag进行统计
* 图片存储在settings.py设置的各个文件夹下
