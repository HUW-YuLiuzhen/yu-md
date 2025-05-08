DeepSeek 本地部署

部署流程  Ollama下载-》deepSeek 安装至ollama -》安装词嵌入模型至ollama



## Ollama 下载：https://ollama.com/

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250209104835356.png" alt="image-20250209104835356" style="zoom:80%;" />

## deepSeek : 打开cmd   输入  ollama run deepseek-r1:14b



## **词嵌入模型**（Word Embedding Model）: 打开cmd   输入 ollama pull shaw/dmeta-embedding-zh

	在 Ollama 或其他机器学习框架中，**词嵌入模型**（Word Embedding Model）是一种将词语映射到低维连续向量空间的技术。以下是其含义和作用：

1. **词嵌入的含义**

词嵌入模型通过训练将词语转换为固定长度的向量，这些向量能捕捉词语的语义和语法关系。常见的模型有 Word2Vec、GloVe、FastText 等。

2. **词嵌入的作用**

- **语义表示**：相似的词在向量空间中距离较近，便于模型理解语义。
- **降维**：将高维的独热编码（one-hot encoding）转换为低维稠密向量，提升计算效率。
- **特征提取**：为文本分类、情感分析等任务提供有效的输入特征。
- **迁移学习**：预训练的词嵌入模型可在不同任务中复用，减少训练成本。

3. 在 Ollama **中安装词嵌入模型**

在 Ollama 中安装词嵌入模型通常包括以下步骤：
1. **选择模型**：如 Word2Vec、GloVe 等。
2. **下载预训练模型**：从公开资源获取预训练的词嵌入文件。
3. **加载模型**：在 Ollama 中加载并使用这些词嵌入。

4. **示例代码**

假设使用 Word2Vec 模型：
```python
from gensim.models import KeyedVectors

# 加载预训练的词嵌入模型
word_vectors = KeyedVectors.load_word2vec_format('path/to/word2vec.bin', binary=True)

# 查询词语向量
vector = word_vectors['apple']
print(vector)

# 计算词语相似度
similarity = word_vectors.similarity('apple', 'orange')
print(similarity)
```

**总结**

词嵌入模型通过将词语转换为向量，帮助模型更好地理解文本语义，广泛应用于自然语言处理任务。在 Ollama 中安装和使用这些模型可以提升文本处理的效果。

​	

## Cherry-Studio：https://cherry-ai.com/download

安装流程：点击 Cherry-Studio-0.9.21-setup.exe 进行安装-》打开 Cherry-Studio 点击设置 -》选择 ollama -》点击管理添加嵌入模型和deepseek模型-》选择进入知识库并对其训练后进行测试

第一步：安装 Cherry-Studio  ，正常安转即可



第二步：打开 Cherry-Studio 点击设置

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250209221648724.png" alt="image-20250209221648724" style="zoom:80%;" />

第三步：选择 ollama

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250209221654877.png" alt="image-20250209221654877" style="zoom:80%;" />

第四步：点击管理添加嵌入模型和deepseek模型

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250209221720889.png" alt="image-20250209221720889" style="zoom:80%;" />

第五步：选择进入知识库并对其训练后进行测试

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250209221859414.png" alt="image-20250209221859414" style="zoom:80%;" />

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250209221959193.png" alt="image-20250209221959193" style="zoom:80%;" />