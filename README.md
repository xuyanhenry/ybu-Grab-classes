# 延边大学yub 抢课爬虫
把选课的主要接口提取出来，省去前端加载界面的时间
使用需要修改代码中请求头的cookies（每次重新登陆都会换），在网页上用cookies查看器产看cookies，要JSESSIONID，SERVERID，如果cookies有两个以上则清空所有cookies重新登陆，这样基本就只剩这两个，把这两个值粘到test_headers中的cookies对应的位置，在程序运行时没有出现Cookies after first request: {'JSESSIONID': ""}这种情况就说明cookies没问题，有Found code: 就说明进选课界面了，如果Cookies after first request:为空然后再不断循环说明没开始选课请求结果为空

选课时根据课程所对应的数字序号进行选择；在140行到180行的内容是检测每个可选课的剩余课程量，在抢课开始时最好屏蔽，要不太占用时间，最好是最后的捡漏排查。

选课输入对应序号后会出现置顶的验证码，输入后 enter后会消失。

在输好验证码后会出现选课结果，选上结果为true,否则为false。

![image](https://github.com/user-attachments/assets/611ca4a9-c76e-4055-ae39-2eeb5097d769)
![image](https://github.com/user-attachments/assets/e849f327-bb86-49ed-892a-a3547cefe764)
