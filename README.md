<h1>基于趋动云平的stable diffusion快速体验</h1><br>
发现一个可以简单轻松体验stable diffusion，平台免费送算力金，不花钱用不完还能白嫖(doge)<br>

<h3>首先，登录趋动云官网：<br></h3>
趋动云官网 <a href="https://account.virtaicloud.com/gemini_web/auth/login">https://account.virtaicloud.com/gemini_web/auth/login</a>，登录趁动云账号（没有账号的话用大陆手机号注册即可）
<img width="800" alt="微信图片_20240709142219" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/11830c05-8b8b-427e-b9c5-029dafe57cba">

<h3>第2步，创建项目：<br></h3>
登录后单击界面右上角的创建项目，“项目名称栏”输入“stable diffusion”，“项目描述”可输入“部署“stable diffusion”。之后点击“确定”<br>
<p align="left">
  <img src="https://github.com/ratchet2118/virtaitech-/assets/128948504/18392685-a7cd-4d08-8e9d-f9c315e0475e" alt="yolo_projCreate" width="800"/>
</p>

<h3>第3步，初始化开发环境：<br></h3>
创建好项目后，在初始化开发环境界面中按照下要求配置开发环境：
资源配置：选择 基础版 中 B1.small。

<p align="left">
  <img width="800" alt="微信图片_20240709152130" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/6f9bbaf1-894b-4089-8116-ce570744d6dc">
</p>

镜像：选择 公开 镜像AUTOMATIC1111/stable-diffusion-webui (作者为“趁动云小助手”)
<p align="left">
  <img width="800" alt="微信图片_20240709153103" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/2b15d4d4-30e6-4890-b1f9-bbff3597b7ab">
</p>

数据选择公开 下的 stable-diffusion-models（作者均为“趋动云小助手”）
<img width="800" alt="微信图片_20240709153734" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/47b99857-316b-4969-92a8-59375f77a3de">

<h3>注意！</h3>点击“公开”选项，否则看不到此镜像、数据集。<br>
带有红星号（镜像的）的必添加1个（镜像）模型、数据、标签等根据不同项目选择性添加。<br>
之后配置高级设置，下拉网页可找到“高级设置”<br>

<p align="left">
  <img width="800" alt="高级设置指示1" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/2436f043-9622-4ac9-80ca-e48543dc54ab">
</p>

点开后按照如下方式来设置即可：
<p align="left">
  <img width="800" alt="微信图片_20240709155307" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/768c450b-e73b-421d-b89d-7a44f6da9195">
</p>
“自动停止”选择8小时，“开放端口”默认为“TCP”，“内部端口”输入“7860”，备注为 “网页形式访问 Stable Diffusion”。<br>
上述都配置好后，点击界面右下角的“立即启动”

<h3>第4步，运行代码：</h3><br>

环境配置好后，单击界面右上角的“进入开发环境”，默认进入 JupyterLab 页面。
<p align="left">
  <img width="800" alt="case_envIn 70fe9289" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/4d2abdbf-a65c-4887-9b35-4fb5c343f597">
</p>

在顶部单击“网页终端”，切换到“网页终端”界面后输入下面的指令：<br>
cd /stable-diffusion-webui/ && python launch.py --deepdanbooru --share --xformers --listen











