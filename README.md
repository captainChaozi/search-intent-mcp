# Search Intent MCP

[![smithery badge](https://smithery.ai/badge/@captainChaozi/search-intent-mcp)](https://smithery.ai/server/@captainChaozi/search-intent-mcp)

请通过 https://aisearchintent.com 获取 API key

这是一个基于 MCP (Model Context Protocol) 的搜索意图分析服务。它可以帮助分析用户搜索关键词的意图，为 SEO 分析提供支持。

## 功能特点

- 分析搜索关键词的意图
- 提供可能的分类
- 提供推理过程
- 提供相关参考链接
- 提供搜索建议

## 使用方法

### Installing via Smithery

To install Search Intent Analysis Service for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@captainChaozi/search-intent-mcp):

```bash
npx -y @smithery/cli install @captainChaozi/search-intent-mcp --client claude
```

### claude 安装

```json
{
  "mcpServers": {
    "search_intent": {
      "command": "npx",
      "args": ["-y", "@search-intent/mcp"],
      "env": {
        "SEARCH_INTENT_API_KEY": "xxx"
      }
    }
  }
}
```

## 开发

```bash
# 克隆仓库
git clone

# 安装依赖
pnpm install

# 设置环境变量
export SEARCH_INTENT_API_KEY=your_api_key
```

## API 使用示例

服务提供了一个名为 `search_intent_analysis` 的工具，可以这样使用：

```json
{
  "name": "search_intent_analysis",
  "arguments": {
    "query": "grok3"
  }
}
```

返回结果示例：

```json
{
  "query": "grok3",
  "intent": "Information Lookup about xAI's Grok 3...",
  "possibleCategories": [
    "AI Model",
    "Technology",
    "Chatbot",
    "Product Information"
  ],
  "reasoning": "The user is likely trying to understand...",
  "references": [
    {
      "url": "https://example.com",
      "title": "Example Title"
    }
  ],
  "searchSuggestions": [
    "grok3 meaning",
    "grok3 search intent",
    "grok3 categories",
    "grok3"
  ]
}
```
