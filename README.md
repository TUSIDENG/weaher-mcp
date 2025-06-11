# mcp weather demo

## 启动服务
### 安装uv
```
# 已安装python时，With pip.
pip install uv

# On macOS and Linux.
curl -LsSf https://astral.sh/uv/install.sh | sh

# On Windows powershell.
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# On Windows Scoop
scoop install main/uv
```

### 使用uv安装python包
```
uv sync
```


## 在cline上配置weather mcp server
1. 进入cline mcp管理界面
![vs code mcp扩展](docs/images/cline%20mcp%20server.jpg)

2. 添加mcp weather配置
如果cline上已有mcp配置，只用将weather部分粘贴到mcpServers配置里面就行
```
{
    "mcpServers": {
        "weather": {
            "command": "uv",
            "args": [
                "--directory",
                "替换为mcp weather项目路径",
                "run",
                "weather.py"
            ]
        }
    }
}
```
![](docs/images/mcp%20weather%20config.jpeg)

# 参考资料
1. mcp weaher demo的建立参考MCP官网[quick start For Server Developers](https://modelcontextprotocol.io/quickstart/server)

2. uv的使用参考
* [Python包管理不再头疼：uv工具快速上手](https://www.cnblogs.com/wang_yb/p/18635441)
* [uv getting-started](https://docs.astral.sh/uv/getting-started/)

3. mcp inspector的使用参考
* [https://github.com/modelcontextprotocol/inspector](https://github.com/modelcontextprotocol/inspector)
* [inspector#getting-started](https://modelcontextprotocol.io/docs/tools/inspector#getting-started)
* [使用Inspector调试MCP服务
](https://www.cnblogs.com/ghj1976/p/18790993/shi-yonginspector-diao-shimcp-fu-wu)