# youngStudy 学习新思想，争做新青年
青年大学习筛选未完成的人员名单

## yt1.0
### 资料准备：
1. 一个班级全部姓名 `.xlxs`表格
2. 一个新的要晒选人员名单的 `.xlsx`表格
> 这两个表格的班级所在的列数要一摸一样，因为是按列来取值

### 安装步骤
1. 下载  `.exe` 文件
2. 下载配置目录 `conf`,放在 `.exe` 的同一级目录
3. 用自己班级的`.xlxs`替换conf 目录下的两个`.xlxs`并改名
4. 修改配置文件信息  `properties.conf`
    1. `all_name_file`是全部人员文件名
    2. `new_name_file`是要筛选的文件名
    3. `index`是班级所在 `.xlsx`中的第几列,从0开始计数
5. 运行 `.exe`
6. 查看`conf`下的`.txt`文件，即为未作人员名单

### 功能
1. 实现了从 `.xlsx` 文件中读取数据
2. 实现了数据的格式化清洗（学号，班级等）
3. 实现了筛选未人完成的人员名单
4. 实现了输出人员名单在`.txt`中

### 缺陷
1. 全部姓名取值和要筛选的人员都是依赖 `.xlsx` 文件,且两个文件的格式要一致
2. 数据的格式化只局限于指定的班级,如果需要修改则要修改源码，重新打包
3. 筛选出的人员名单没有进行持久化处理,后期无法统计次数
5. 只做了筛选人员名单作用，没有真正实现提醒功能