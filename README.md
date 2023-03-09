# APISpace 介绍
**本 API 服务由 [APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=chatgpt) 提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：
- Java(OK HTTP)
- HTTP
- cURL
- 微信小程序
- PHP(pecl_http)、PHP(cURL)
- Python(http.client)、Python(Requests)
- JavaScript(Jquery AJAX)、JavaScript(XHR)
- NodeJS(Native)、NodeJS(Request)
- Ruby(Net:Http)
- Shell(Httpie)、Shell(cUrl)

# OpenAI-ChatGPT
OpenAI 的 Davinci 模型 GPT-3.5 的 API， 能够模拟人类的语言行为，与用户进行自然的交互。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/chatgpt/introduction](https://www.apispace.com/eolink/api/chatgpt/introduction?utm_source=github&utm_term=chatgpt) 申请API服务**

本文档末尾提供了 Python(Requests) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/eolink/api/chatgpt/guidence/](https://www.apispace.com/eolink/api/chatgpt/guidence/?utm_source=github&utm_term=chatgpt)

**使用注意事项：** 严禁提问政治敏感信息，请遵守相关法律法规。目前该API可 **正常调用**。

为了方便广大国内开发者体验最新的 ChatGPT 能力，APISpace 通过官方渠道直接接入 OpenAI 的 Davinci 模型 GPT-3.5 的 API。

注册 APISpace 即可免费获得 10 次调用，并且无需注册 OpenAI 海外账号、无需海外信用卡、快速测试、快速接入。

温馨提示：体验 ChatGPT 本体 API，点击试用 [ChatGPT-3.5 Turbo API](https://www.apispace.com/eolink/api/chatgpt-turbo/introduction?utm_source=github&utm_term=chatgptturbo)

### 扣费标准

1.  OpenAI 目前把单次的 **提问+回答** 限定在 4096 Tokens 以内，1 token=0.5个汉字=2个英文字符。也就是单次的提问+回答最多约 2048 个汉字的长度。
1.  由于 OpenAI 的访问量激增，OpenAI 服务商偶现超时的情况，此时会导致返回超时，**超时不扣费**。

### ChatGPT 介绍

ChatGPT 是一款由 OpenAl 开发的语言模型产品，它能够模拟人类的语言行为，与用户进行自然的交互。ChatGPT 基于GPT-3.5（Generative Pretrained Transformer 3.5）的语言模型建造，通过使用大量的训练数据来模拟人类的语言行为，并通过语法和语义分析，生成人类可以理解的文本。它可以根据上下文的语境，提供准确和恰当的回答，并模拟多种情绪和语气，可以让用户在与视器交互时，感受到更加真实和自然的对话体验。
![image](https://user-images.githubusercontent.com/36323798/223967231-35ceb770-3811-48f9-b59d-7ac07ff4ae22.png)


### 应用场景

1.  非结构化对话：ChatGPT 3.5可以应用于基于对话内容的推断和问答，如在技术支持、客户服务等场景中，快速回复访客提出的各种查询;
1.  智能客服：ChatGPT 3.5可以作为基于智能聊天机器人的客服，具备自动响应技能，可以自动预测和解决客户的问题；
1.  情绪分析：ChatGPT 3.5可用于客户交互过程中的情绪分析，分析客户的语义以及语气从而深入了解客户的隐含情绪和感受；
1.  信息检索：ChatGPT 3.5可以应用于从海量数据中提取信息和知识的过程，提升信息获取和检索效率；
1.  社交媒体分析：ChatGPT 3.5可以应用于社交媒体数据挖掘，分析影响用户决策的信息，从而更好地洞察客户的利益和需求；
1.  自然语言处理：ChatGPT 3.5可以应用于复杂的自然语言处理，如自动文本翻译，文本分类，文本生成等。


### 免责声明

本服务仅供个人学习、学术研究目的使用，未经许可，请勿分享、传播输入及生成的文本、图片内容。您在从事与本服务相关的所有行为（包括但不限于访问浏览、利用、转载、宣传介绍）时，必须以善意且谨慎的态度行事；您确保不得利用本服务故意或者过失的从事危害国家安全和社会公共利益、扰乱经济秩序和社会秩序、侵犯他人合法权益等法律、行政法规禁止的活动，并确保自定义输入文本不包含违反法律法规、政治相关、侵害他人合法权益的内容。

### Python(Requests) 调用代码示例

```
import requests

url = "https://eolink.o.apispace.com/chatgpt/create"

payload = {"text":""}

headers = {
    "X-APISpace-Token":"",
    "Authorization-Type":"apikey",
    "Content-Type":""
}

response=requests.request("POST", url, data=json.dumps(payload), headers=headers)

print(response.text)

```
