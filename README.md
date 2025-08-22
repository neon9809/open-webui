# [Open WebUI 👋](https://github.com/open-webui/open-webui)

![GitHub stars](https://img.shields.io/github/stars/open-webui/open-webui?style=social)
![GitHub forks](https://img.shields.io/github/forks/open-webui/open-webui?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/open-webui/open-webui?style=social)
![GitHub repo size](https://img.shields.io/github/repo-size/open-webui/open-webui)
![GitHub language count](https://img.shields.io/github/languages/count/open-webui/open-webui)
![GitHub top language](https://img.shields.io/github/languages/top/open-webui/open-webui)
![GitHub last commit](https://img.shields.io/github/last-commit/open-webui/open-webui?color=red)
[![Discord](https://img.shields.io/badge/Discord-Open_WebUI-blue?logo=discord&logoColor=white)](https://discord.gg/5rJgQTnV4s)
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/tjbck)

**Open WebUI is an [extensible](https://docs.openwebui.com/features/plugin/), feature-rich, and user-friendly self-hosted AI platform designed to operate entirely offline.** It supports various LLM runners like **Ollama** and **OpenAI-compatible APIs**, with **built-in inference engine** for RAG, making it a **powerful AI deployment solution**.




## Open WebUI Auth Footer

在官方v0.6.25基础上增加了在/auth页面添加Footer的功能

引入了：
 - src/lib/components/RegistrationInfo.svelte

修改了：
 - src/routes/auth/+page.svelte
 - backend/open_webui/config.py
 - backend/open_webui/main.py

Dockerfile添加了：

RUN mkdir -p /app/backend/data/static && chown -R $UID:$GID /app/backend/data/static

VOLUME ["/app/backend/data/static"]

### 使用：

将需要添加的Footer内容写入 ./static/registration.html
然后在docker-compose或docker run中添加 "./static:/app/backend/data/static:ro"

docker镜像只有Linux/amd64版本 

## [商业部署须从OpenWebUI官方获取商业授权](https://docs.openwebui.com/enterprise/)

