# How2UseNotebookLLM2Study

## 2025/12 实测谷歌NotebookLM最佳学习工具记录 https://notebooklm.google.com/ ；🔴**基于最新最强模型 Gemini3Pro（GPT4.6档+） 和 Banana3Pro，文本/多模态理解和PPT图的生成已经接近满分，图片表达清晰准确，还有故事线串起来被惊艳到了，个别汉字小字体时生成还有些问题；总分给到19分！！！

- 输入原始材料：G3英语单元复习资料 8个单词+5个词组+3个句子+2给语法知识点 = 2页Word内容
- 输出：
  1. **Slide Deck（精华）：PPT可下载Pdf**，总体评价文本9.5分+图/格式9.5分；内容只漏1个词组约4%，还有故事串起+格式完美，画错1页中5处中文；**可写提示词进一步控制**
  2. **Video（精华）：视频输出本身就不错可下载MP4**，如果先输出Slide Deck再Video就是该PPT的最好讲解；**可写提示词进一步控制**
  3. **InfoGraphic（精华）:单页精华PPT，可下载PNG**
  4. Mindmap：思维导图可下载PNG
  5. FlashCard：闪卡帮助记忆重要概念，可下载CSV格式
  6. Quiz：可共享的测试（_能看到原始Notebook_）；例如https://notebooklm.google.com/notebook/a5180ed6-6f73-4117-a127-4dcd4b940589?artifactId=ea6cdaec-3789-4c43-b978-2f6faea5e5fe
  7. Audio：Video的播客版；**甚至还有Interactive模式可以和2个主持人对话**
  8. Report：把原始文档根据你的提示词进行文本转化；例如摘要、学习指南或Blog等
- 限额：免费账户精华的都limited，Video/Audio 3次/天，AI Pro账户约X3；https://support.google.com/notebooklm/answer/16213268

## 2025/12 实测密塔 - 专题（新） 国内最佳学习工具记录 https://metaso.cn/subject-v2 🔴MetaSo的Nano Banana2还可以给7-8分，图片表达很一般，文本生成也有不少问题但勉强能用；但指令跟随漏文本约10-22%，只能给6-7分；总分给到14分
- 输入原始材料：G3英语单元复习资料 8个单词+5个词组+3个句子+2给语法知识点
- 输出：
  1. **“给我讲讲”（精华）：先转成PPT然后讲解**，下载PPT和视频要付费，速讲+3D风格时文本6分+图/格式8分/**课堂+3D风格**时文本7分+图/格式8分； **讲完视频有个“考考我”的测试**，分享后看不见原文，例如https://metaso.cn/api/s/pObSxPn
  2. **创建海报（精华）：生成总结性HTML网页可进一步做PPT，没有调用Banana生图，而用字体风格来做所以文本完全正确，内容漏20%给6分，形式给8分**；例如https://metaso.cn/api/s/w3SWNqu

## 2025/12 实测用GPT5.2 Extended Think 用提示词手工搓了一个PPT，🔴文本给到9.5分内容未漏，比NotebookLM只少故事串起来但是真PPT可以自己改，图片以Icon为主/格式表达不错给8-9分；总分给到18分！
- 输入原始材料：G3英语单元复习资料 8个单词+5个词组+3个句子+2给语法知识点
- 使用了以下Prompt，该提示词是NotebookLM的缺省Slide Deck的
```bash
对于我上传的文件。使用中文制作一个PPT形式的Detailed Deck（A comprehensive deck with full text and details, perfect foremailing or reading on its own. ）帮助我学习我上传的文件。Add a high-level outline, or guide the audience, style, and focus: "Create a deck for beginners using a bold andplayful style with a focus on step-by-step instructions."。形成PPT文件，供我下载
```

## Pdf转PPT的高质量免费工具

- [PdfGear Online直接用](https://www.pdfgear.com/pdf-to-pptx/) ，效果⭐⭐⭐，大致能拆解，但字和排版还是有些问题，后续手工有不少调整；原始文件100MB以内
- 使用下载后的PdfGear把Pdf转PPT，格式完美但都是图片本身，无法编辑。**可以采用这个方法结合上面的修改个别页面上的文字**

- https://www.ilovepdf.com/zh-cn/pdf_to_powerpoint 免费版通常有每日次数限制（每天 1-2 次）；老牌“装机必备”；效果⭐⭐⭐，与PdfGear Online类似
- 在只输出图片没有文字框的情况下，只用用Qwen3Max 图像编辑工具用类似如下Prompt修图来做。

#### 原图
<img width="1146" height="640" alt="image" src="https://github.com/user-attachments/assets/39312aad-8fdf-4860-a33a-6a166798f974" />

#### 只用Qwen3Max编辑图片，去掉右下角的文字。只做一次，图片还能看
<img width="1146" height="640" alt="image" src="https://github.com/user-attachments/assets/1d7a2219-e0bd-48b3-bdd6-a6755325ea46" />

#### 用Qwen3Max编辑图片，因为一次修改多处文字，文字都会不正确，所以每次修改文字2处，共做了3次，图片明显变糊对比度也不够
```bash
Prompt
把红框中的文字变成：你想和他们一起去吗？
把蓝框中的文字变成：我能摸一下它吗？
去掉右下角的文字
```
<img width="1146" height="640" alt="image" src="https://github.com/user-attachments/assets/798258a6-27a9-41a9-bdd6-47f537fa9f2b" />


-【ToDo】
1. Adobe Acrobat 在线版 (还原度之王)
作为 PDF 格式的发明者，Adobe 的算法对“逆向转换”做得最好。它能精准识别原 PPT 的文本框、背景图和层级关系。

优势：转换出的 PPT 最像原生文件，文字不会乱码，位置偏离极小。

免费情况：支持在线免费转换，但每天有次数限制（通常 1-2 次）。

网址：Adobe Acrobat PDF to PPT

**2、氪金的WPS VIP，pdf转PPT不知效果如何**

3. Canva 可画 (二次编辑神器)
如果你不仅想转回 PPT，还觉得原来的设计有点老旧，想顺便美化一下，选 Canva。

用法：将 PDF 上传到 Canva，它会利用 AI 自动拆解 PDF 的元素。你可以直接在 Canva 里拖拽修改，完成后点击“分享”->“更多”->“下载为 Microsoft PowerPoint”。

优势：排版自由度极高，适合把死板的 PDF 变成现代化的幻灯片。

网址：canva.cn (国内版) 或 canva.com (国际版)
