# CopilottoGPT4
1.copilot-gpt4-service，它可以将 Github Copilot 转换为 ChatGPT，将使得你可以通过 ChatGPT-Next-Web 的第三方客户端，免费使用ChatGPT进行对话，前提是您需要有copilot的使用权限。原理是Github Copilot其实是调用的OpenAI的服务。<br><br>
2.GitHub Copilot 服务只有学生可以免费认证开通（若注册遇到问题可以查看该文档https://zhuanlan.zhihu.com/p/623326208）<br><br>
3.成功之后得到一个导出一个token。如ghu_iEzI6rem7vZoQ68opqruA0h7aaULXM2UfC8D格式（该token是伪造的，真实token不可随意共享）<br><br>
4.下载windows版本的docker（https://www.docker.com/）<br><br>
5.在命令行一键部署<br>
```
docker run -d \
--name copilot-gpt4-service \
--restart always \
-p 8080:8080 \
-e HOST=0.0.0.0 \
aaamoon/copilot-gpt4-service:latest
```
<br>
6.一键部署ChatGPT-Next-Web

```
docker run -d \
--name copilot-gpt4-service \
--restart always \
-p 8080:8080 \
-e HOST=0.0.0.0 \
aaamoon/copilot-gpt4-service:latest
```

7.部署之后的效果图<br>
![Example Image](https://github.com/wewelucky/CopilottoGPT4/blob/main/docker.png)<br>
8.启动后，可以在本地 http://127.0.0.1:8080  来访问 copilot-gpt4-service 服务。<br><br>
9.安装完成后，在浏览器中用'http://localhost:3000/'即可访问，但是这只是本地的方法，别人无法访问。<br><br>
10.然后设置模型，接口地址和token，如下图<br>
![Example Image](https://github.com/wewelucky/CopilottoGPT4/blob/main/setting.png)<br>
11.然后测试一下和3.5之间的区别<br>
3.5：<br>
![Example Image](https://github.com/wewelucky/CopilottoGPT4/blob/main/test1.png)
<br>
4.0:<br>
![Example Image](https://github.com/wewelucky/CopilottoGPT4/blob/main/test2.png)
<br>

