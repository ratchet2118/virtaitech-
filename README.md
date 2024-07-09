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
<p align="left">
  <img width="800" alt="chatglm-6_inTerminal 47d6e444" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/44433b76-d86b-42ce-a912-271f714c54a4">
</p>

情况1：代码运行结果显示出网址，如下所示：<br>
<p align="left">
  <img width="800" alt="sd_publicUrl d6f63e28" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/4e5a1956-d721-4fc0-8779-054d32105423">
</p>
即可直接复制网址访问；<br>

情况2：运行后不显示网址，如下所示：<br>
<p align="left">
  <img width="800" alt="端口指示" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/6edc9fc6-819b-4afc-ab30-721ca1cd7150">
</p>
单击界面右侧的端口，复制外部访问的链接打开，若不行则开启浏览器的“无痕浏览模式”或切换Microsoft Edge访问。

<h3>第5步，使用模型：</h3><br>
<p align="left">
  <img width="800" alt="sd_web 6c58161d" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/8f8eec66-0629-4b26-b777-3af56dcfd946">
</p>
 “Prompt”栏中输入的关键词为想要生成的内容，“Negative prompt”中输入的关键词为不想出现的内容。<br>
可在下方调整生成图片的一系列参数：Sampling method--采样方法不同模型适配的方法不一样，一般大同小异；Sampling steps--采样步数diffusion step步数，一般取值在[10.20]，小于10效果太差，大于20提升不明显，但是为了最求极致也可以设置更高(如40)；Width\Height--分辨率生成的图片分辨率。默认512*512，但是太小。太小会限制模型发挥:也不要太大，太大跑不动。Batch size--每批数量bs，多了爆显存。

<h3>更换模型</h3><br>
Stable Diffusion 部署后，默认只有一个模型可选择和使用，参考如下步骤，加载更多模型：<br>
1、	切回JupyterLAB界面（切勿关闭部署时的网页终端页面）<br>
2、	单击 + new Launcher，随后在新的 Launcher 页单击 Terminal，新建终端。<br>
<p align="left">
  <img width="800" alt="sd_newTerminal 9f538a8f" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/8f4914f2-14a9-40cb-ae41-7776cf6024ae">
</p>
3、在新开的终端中执行如下命令：<br>
ln -s /gemini/data-1/novelaileak/ /stable-diffusion-webui/models/Stable-diffusion/<br>
4、返回Stable Diffusion 页面，刷新 checkpoint 下拉框，加载出更多模型：<br>
<p align="left">
  <img width="800" alt="sd_checkpointRefresh 3b021d99" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/5a423c7d-da2d-4a6a-bc47-9df7cacf4a91">
</p>

<img width="800" alt="微信图片_20240709171101" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/c8c0a2d1-546e-4e1a-85d5-8ef117ea2f05">

刷新、更换模型可能耗费一定时间，stable diffusion运行一段时间后，注意“网页终端”里是否出现报错：Connection Reset By Peer! Try Refresh，此时需要刷新网页终端，重新运行程序，复制并打开新的链接
<p align="left">
  <img width="800" alt="image" src="https://github.com/ratchet2118/virtaitech-/assets/128948504/a321ffe8-62db-4ecf-bffd-d4346a2f5dce">
</p>

















