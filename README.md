# IP情报查询工具 IP Search

依托全球蜜罐网络及百万级节点构建的IP情报分析平台，提供精准的IP画像与威胁预警服务。
Relying on a global honeypot network and an IP intelligence analysis platform built with millions of nodes, it provides precise IP profiling and threat early warning services.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| 长亭 IP 情报查询 | 基于长亭威胁情报，获取给定 IP 的威胁情报信息，包括 IP 地址、地理位置、ASN、历史恶意行为等信息 |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659365891](https://mcp.xiaobenyang.com/inspector/1777316659365891)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659365891](https://mcp.xiaobenyang.com/inspector/1777316659365891)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "IP情报查询工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659365891/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "IP情报查询工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659365891/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "IP情报查询工具": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659365891",
          },
          "transport": "stdio"
        }
      }
}

```
