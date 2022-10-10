# DrivingTestSubjectOne
题库源: banban驾道
题库最后更新：2022/07/17

## 查询
安装python3任意版本，进入项目目录
`python main.py`

# 本题库仅供学习，便于考生快查快记，严禁用于考试作弊等违法犯罪行为！！！
--------------2022年10月10日14点06分------------

关于我的更新部分  

个人有强迫症，这位朋友爬取的题库图片jpg部分链接后缀带着"jpg?imageslim"字样，看着十分难受。  
比如"url": "http://app.static.public.chetailian.com//exam/subject1/2019_kemu1_806400.jpg?imageslim"。

用Linux的sed命令替换掉q.json里面的所有"?imageslim" :  `sed 's/?imageslim//' q.son`

然后用cat命令把q.json里面的所有图片链接(http链接)匹配出来导入到img.txt文件里: `cat q.json |tr '"' '\n' | tr "'" '\n' | grep -e '^https://' -e '^http://' -e'^//' | sort | uniq >> img.txt`

最后用·wget -i img.txt·，把所有http链接图片下载到本地，方便离线使用。
