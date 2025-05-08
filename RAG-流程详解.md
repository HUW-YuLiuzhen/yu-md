# RAG详细流程详解

## 一、离线步骤：

1. 文档加载

2. 文档切分

3. 向量化

4. 灌入向量数据库

## 二、在线步骤：

1. 获得用户问题

2. 用户问题向量化

3. 检索向量数据库

   ​	**Chroma 向量数据库**  官方文档：https://docs.trychroma.com/docs/overview/introduction

   ​	

4. 将检索结果和用户问题填入 Prompt 模版

5. 用最终获得的 Prompt 调用 LLM

6. 由 LLM 生成回复

<img src="G:\聚客AI学习资料\16项目实战三期\2_RAG-Embedding-Vector\day02\RAG-Embeddings\assets\rag.png" style="zoom:67%;" />