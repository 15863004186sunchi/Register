# Grok (x.ai) 注册机使用教程

## 环境准备

1. 创建并激活虚拟环境（Python 3.10+）：

```bash
cd grok-register
python3 -m venv venv
source venv/bin/activate    # Windows 用 venv\Scripts\activate
```

2. 安装依赖：

```bash
pip install curl_cffi beautifulsoup4 requests python-dotenv
```

3. 准备输出目录：

```bash
mkdir -p keys
```

4. 配置文件：
   - 复制 `.env.example` 为 `.env`
   - **YESCAPTCHA_KEY**: YesCaptcha 的 API Key（必需，用于过 Turnstile）
   - **DUCKMAIL_BEARER**: DuckMail 的 API Token（必需，用于自动创建临时邮箱）
   - **GROK_ACTION_ID**: (可选) 若程序自动获取失败，可手动填写从浏览器抓取的 Action ID

```env
YESCAPTCHA_KEY="你的_yescaptcha_key"
DUCKMAIL_BEARER="你的_duckmail_bearer"
```

## 运行

```bash
cd grok-register
source venv/bin/activate
python grok.py
# 提示输入并发数，回车默认 8
```

成功后输出：

- `keys/grok.txt`：SSO token 列表 (用于直接登录)
- `keys/accounts.txt`：email:password:SSO 相关账号信息

## 进阶功能

- **指纹轮换**: 程序内置了 Chrome, Safari, Firefox, Edge 等多种浏览器指纹，自动尝试最通畅的路径。
- **Cloudflare 绕过**: 针对 GCP 等机房 IP 可能遇到的 403 拦截，程序会自动解析 `next-action` ID。若完全被锁，支持通过 `.env` 手动填入 ID。
- **邮件服务**: 已集成 DuckMail 自动注册接口，支持 `XXX-XXX` 格式验证码自动提取。

## 注意事项

- 必须确保 YesCaptcha 账户有余额。
- 建议使用高质量代理以降低被 Cloudflare 拦截的概率。
- 若提示“未找到 Action ID”，请参考 [IMPLEMENTATION.md](./IMPLEMENTATION.md) 进行手动抓取。
