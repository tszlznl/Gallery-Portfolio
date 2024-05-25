# Gallery-Portfolio

## 部署步骤

1. 将 `.env_template` 改名为 `.env`，并修改其中的配置
2. 使用以下方法部署：

```console
npm init -y
npm install @aws-sdk/client-s3 sharp dotenv express exif-parser
node server.js
```

## Progress Flow

- [x] 正常显示 Cloudflare R2 bucket 某个路径下的所有图片
- [x] 点击图片展示大图
- [x] 日夜间模式切换按钮
- [x] 大图显示对应的 exif 信息
- [x] 每页底部有点击加载的按钮，加载下一页的图片，并保留显示之前的所有图片
- [x] 在底栏增加版权信息和外链
- [x] 页面标题栏美化，改名并加顶栏，以便后续放标签等信息
- [x] 每页最少显示 2 列图片，并随着页面宽度的增加，逐步增加显示的列数，最多显示 6 列图片，在页面宽度增加的时候保持列宽不变；如果显示到 6 列之后屏幕宽度仍然继续增加，则在页面左右两侧增加空白。
- [x] 根据显示列数动态调整每页加载的图片数量
- [x] 创建缩略图以供预览加载
- [ ] 加入标签系统，使用标签筛选图片
- [x] 压缩图片的过程中保留原图的 metadata 信息，使图片的旋转方向正常
- [x] 在 R2 目录下所有图片都加载完成后，把“加载更多”按钮的文字替换为“已全部加载”，并变成灰色不可点的状态
- [ ] 在顶栏 GitHub 按钮左侧，加入一个按钮，可以切换页面滚动到底部自动点击“加载更多”按钮或不自动点击。
- [ ] 在代码上优化，加快 exif 信息的加载速度。比如让图片和 EXIF 信息并行加载；仅加载需要显示的 exif 信息
