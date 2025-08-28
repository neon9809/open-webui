## v0.6.26更新

### 文件修改：

- `/src/routes/auth/+page.svelte` ————加入footer模块
- `/Dockerfile` ————将外部registration.html 映射到容器内

### 使用方法：

通过`docker- compose`或`docker run` (`container run`)映射文件进容器：
"/path/to/your.html:/app/backend/open_webui/static/registration.html:ro"