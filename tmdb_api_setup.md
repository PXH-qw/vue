# TMDb API 配置说明

## 获取TMDb API密钥

要使用TMDb（The Movie Database）API获取真实的电影海报，请按以下步骤操作：

1. 访问 [TMDb官网](https://www.themoviedb.org/)
2. 注册一个账户（如果还没有的话）
3. 登录后访问 [API设置页面](https://www.themoviedb.org/settings/api)
4. 申请开发者API密钥
5. 选择"Developer"账户类型
6. 填写应用信息并提交申请
7. 申请通过后，你会获得一个API密钥

## 配置API密钥

### 方法一：环境变量（推荐）

1. 在项目根目录创建 `.env` 文件
2. 添加以下内容：

```
VUE_APP_TMDB_API_KEY=你的API密钥
```

3. 重新启动开发服务器

### 方法二：直接修改代码

1. 打开 `src/utils/tmdbApi.js` 文件
2. 找到 `const API_KEY = process.env.VUE_APP_TMDB_API_KEY || 'YOUR_API_KEY_HERE';` 这一行
3. 将 `'YOUR_API_KEY_HERE'` 替换为你的实际API密钥
4. 保存文件

## 注意事项

- API密钥是私密信息，请不要提交到版本控制系统中
- 在 `.gitignore` 文件中添加 `.env` 以避免泄露密钥
- TMDb API有请求频率限制，请合理使用

## 故障排除

如果仍然显示 `vite.svg` 图片：
1. 检查API密钥是否正确配置
2. 确认网络连接正常
3. 检查TMDb API是否正常工作
4. 查看浏览器控制台是否有错误信息

## 替代方案

如果TMDb API无法使用，系统会自动回退到使用Picsum.photos提供的随机图片，确保应用正常运行。