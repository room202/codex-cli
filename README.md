# Codex CLI

[公式サイト](https://developers.openai.com/codex/cli)

[公式GitHub](https://github.com/openai/codex)

## 前提条件

- [Node.js 18+](https://github.com/room202/react?tab=readme-ov-file#volta-%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
- [Git 2.23+](https://git-scm.com/)
- [GitHub CLI](https://github.com/cli/cli)

## インストール

```bash
npm install -g @openai/codex
```

## 実行

```bash
codex
```

## MCP

### 設定ファイル

フォルダ : `C:\Users\%USERPROFILE%\.codex`

ファイル : `config.toml`

### Serena

#### 事前準備

Window11

```ps
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

macOS

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### 設定内容

```toml
[mcp_servers.serena]
command = "uvx"
args = [
    "--from",
    "git+https://github.com/oraios/serena",
    "serena",
    "start-mcp-server",
    "--context",
    "codex"
]
# 環境変数を明示
env = { SystemRoot = "C:\\Windows", windir = "C:\\Windows" }
```
