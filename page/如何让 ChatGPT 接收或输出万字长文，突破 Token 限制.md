ChatGPT 强大的自然语言处理能力令人惊叹，但其 Token 限制却让许多用户感到困扰。尽管 Claude 2 的 Token 容量更大，但 ChatGPT 的用户群体仍然占据主导地位。本文将介绍如何突破 Token 限制，帮助你上传更长的文本并让 ChatGPT 输出万字长文。通过实际案例，你将学会如何操作，充分释放 ChatGPT 的潜力。

## 为什么 ChatGPT 有 Token 限制？

人类通常以字数计算文本长度，而大语言模型（LLM）则使用 Token 来分解句子。Token 可以是一个单词、单词的一部分，甚至是一个字符，具体取决于标记化方法。例如，句子 “ChatGPT is great!” 可能会被分解为 [“Chat”, “G”, “PT”, “is”, “great”, “!”] 这 6 个 Token。

你可以使用 [OpenAI 的 Tokenizer](https://platform.openai.com/tokenizer) 工具将 Token 数换算为字符数，或者参考以下近似公式：

- 1 个 Token ≈ 4 个英文字符  
- 1 个 Token ≈ ¾ 个英文单词  
- 100 个 Token ≈ 75 个英文单词  

Token 限制包括输入和输出内容。例如，ChatGPT 3.5 的 Token 限制是 4096，ChatGPT 4 的 Token 限制是 8192。这种限制主要与内存和计算效率有关。GPU 或 TPU 的物理内存限制会导致超出 Token 限制的操作失败或变得极其缓慢。此外，随着 Token 数量增加，计算量也会显著增加，从而影响响应速度。

尽管如此，许多场景下我们仍需要提交长文本或生成长文内容，例如总结一本书或撰写长篇论文。

## 如何提交超过 Token 限制的文本？

以下方法可以帮助你提交超长文本：

1. **使用更大 Token 容量的模型**  
   在 OpenAI Playground 中选择如 “GPT-4.5-turbo-16k” 或 “gpt-4-32k” 的模型（需额外付费）。

2. **分段上传文本**  
   提前告知 ChatGPT 你将分段上传内容，例如：  
   > “The text that I’m about to submit will be divided into several parts. I request that you wait until all parts have been provided before summarizing or answering any questions about it.”  
   上传完成后再提问或分配任务。

3. **使用浏览器插件**  
   借助谷歌浏览器插件 **ChatGPT File Uploader Extended**，自动将长文本分割并依次上传。

4. **上传 PDF 文件**  
   将内容保存为 PDF 文件并使用工具如 AskYourPDF 上传。

5. **使用代码解释器**  
   将文本保存为记事本文件，通过 ChatGPT 的代码解释器上传。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)

## 如何让 ChatGPT 的输出突破 Token 限制？

以下方法可以帮助你生成超长文本：

1. **使用“Continue”按钮**  
   当 ChatGPT 的响应因 Token 限制中断时，点击“Continue”按钮继续生成内容。

2. **手动输入“Continue”**  
   如果没有按钮，直接输入“Continue”让 ChatGPT 继续未完成的响应。

3. **指定字数或字符数**  
   明确要求 ChatGPT 输出特定字数的内容，例如：  
   > “写一篇 1 万字有关生成式 AI 的论文。”

4. **分段输出**  
   如果内容超出 Token 限制，ChatGPT 会主动分段输出，你只需让它继续即可。

5. **列提纲分步生成**  
   让 ChatGPT 先列出提纲，然后根据提纲逐步生成每个部分的内容。

## 实际案例演示

以下是一个实际案例：将 YouTube 上哈佛大学关于 GPT-4 的 55 分钟讲座（字幕文本超 1 万字）转化为详细笔记。

### 步骤

1. **获取字幕文本**  
   使用 **YouTube Summarizer with ChatGPT** 插件复制视频字幕文本并保存为文本文档。

2. **分段上传**  
   激活 **ChatGPT File Uploader Extended** 插件，将文本分割后依次上传。

3. **分配任务**  
   上传完成后，使用以下提示词让 ChatGPT 转换为笔记：  
   > “我想把您之前的所有回复（YouTube 文字记录）转换成一份全面的 Obsidian 笔记，目标字数约为 10,000 字。请先创建一个大纲，将记录稿分成几个部分，说明每个部分的预计字数。”

4. **生成提纲**  
   ChatGPT 会根据字幕内容生成提纲，例如：  
   - 引言（400 字）  
   - 语言模型和 GPT-4（800 字）  
   - 写作 Atlas 项目（750 字）  
   - 构建人工智能生成的实用应用程序（1300 字）  
   - 处理幻觉和提高准确性（1200 字）  
   - 应用和商业价值（1100 字）  
   - 隐私和知识产权考虑（900 字）  
   - GPT-4 在未来计算中的作用（900 字）  
   - 结论（400 字）

5. **逐步生成内容**  
   按照提纲逐步生成每个部分的内容，确保细节完整。

6. **完成笔记**  
   最终生成的笔记虽然未达到 10,000 字，但已非常详细。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)

## 小结

ChatGPT 的 Token 限制可能会对处理大量内容的用户造成不便，但通过分段上传、设计提示词或使用插件等方法，可以有效突破这一限制。理解并适应这些限制后，你将能够充分发挥 ChatGPT 的强大能力，为各种任务提供支持。