## LangChain 与 LlamaIndex 的错位竞争

- LangChain 侧重与 LLM 本身交互的封装
  - Prompt、LLM、Message、OutputParser 等工具丰富
  - 在数据处理和 RAG 方面提供的工具相对粗糙
  - 主打 LCEL 流程封装
  - 配套 Agent、LangGraph 等智能体与工作流工具
  - 另有 LangServe 部署工具和 LangSmith 监控调试工具
- LlamaIndex 侧重与数据交互的封装
  - 数据加载、切割、索引、检索、排序等相关工具丰富
  - Prompt、LLM 等底层封装相对单薄
  - 配套实现 RAG 相关工具
  - 有 Agent 相关工具，不突出
- LlamaIndex 为 LangChain 提供了集成
  - 在 LlamaIndex 中调用 LangChain 封装的 LLM 接口：https://docs.llamaindex.ai/en/stable/api_reference/llms/langchain/
  - 将 LlamaIndex 的 Query Engine 作为 LangChain Agent 的工具：https://docs.llamaindex.ai/en/v0.10.17/community/integrations/using_with_langchain.html
  - LangChain 也 _曾经_ 集成过 LlamaIndex，目前相关接口仍在：https://api.python.langchain.com/en/latest/retrievers/langchain_community.retrievers.llama_index.LlamaIndexRetriever.html

