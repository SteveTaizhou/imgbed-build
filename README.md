# 手把手教你用 GitHub 和 PicGo 自建私人图床

参考文章：[使用Github+picGo搭建图床，保姆级教程来了](https://zhuanlan.zhihu.com/p/489236769 "知乎")

仓库：`SteveTaizhou/s-imgbed`

## 0 准备工作

一台电脑，一个 GitHub 账号，一个人。

打开 GitHub，网址：<https://github.com/>。登录（或许要先注册）。

## 1 仓库搭建

在屏幕右上角点击加号，在下拉菜单中点击 New repository，也可以直接去<https://github.com/new>。

![图片](https://user-images.githubusercontent.com/85382878/185338583-ac38d05c-7bc5-436e-9e66-6adb47748c57.png)

在页面中上面一个红色方框所示的位置填写仓库名称，不要用中文。在右边显示勾勾的时候就可以了。建议勾选复选框，添加 README.md 文件，内容自动生成，可以更改。

![图片](https://user-images.githubusercontent.com/85382878/185338957-6b0dc1cd-81e4-4807-867d-369849f4cb8b.png)

如果你填入空格之类的东西，会弹出黄色方框，加粗内容表示最终仓库名称。

![图片](https://user-images.githubusercontent.com/85382878/185340002-9286bb8a-e7e2-442b-8566-bd8980950e6b.png)

**注意** 起名的时候要让仓库名尽量的短，因为这会直接出现在最终的图片 URL 中。

滚动到最底部，点击绿色按钮即可。耐心等待。

![图片](https://user-images.githubusercontent.com/85382878/185340479-af421674-281f-44b5-bb06-bd78ef18d935.png)

**提示** 可以简单的进入<https://github.com/SteveTaizhou/s-imgbed/fork>直接 fork 本仓库。

完成后，复制页面 URL 中 `https://github.com/` 后面的部分，我们把他叫做 _path_。

## 2 令牌生成

点击用户头像，在下拉菜单中点击 Settings。

![图片](https://user-images.githubusercontent.com/85382878/185341074-9f7b7b41-efd8-49a0-9dc6-b3b936daa8fa.png)

在左侧菜单中点击 Developer settings，应该在最底部。

![图片](https://user-images.githubusercontent.com/85382878/185341507-f5efc384-1bea-4492-9b3d-2bddb61aa727.png)

然后在左侧菜单中点击 Personal access tokens。

![图片](https://user-images.githubusercontent.com/85382878/185341803-8b63c7d0-c031-4f10-85be-2c972045a1da.png)

点击 Generate new token。

![图片](https://user-images.githubusercontent.com/85382878/185342051-cd13bfd5-8b3d-4b3f-aec4-01f50ae607e5.png)

此时页面 URL：<https://github.com/settings/tokens/new>。

![图片](https://user-images.githubusercontent.com/85382878/185343047-3ac3fc95-7175-44ef-b00a-bbaa3083ed23.png)

1. 表示用途。
2. 表示有效期。
3. 必须勾选。

下拉菜单内容：

![图片](https://user-images.githubusercontent.com/85382878/185343468-592549af-84dc-4ba9-9561-2721fcbba4ce.png)

完了以后点击页面底部的绿色按钮。

![图片](https://user-images.githubusercontent.com/85382878/185343710-a4d24e5a-69e9-4393-8c89-c26e795582be.png)

复制红色框框所标识的文本。妥善保存，这很重要，以后还会用到。我们把他叫做 _token_。刷新页面就看不到了。

![图片](https://user-images.githubusercontent.com/85382878/185344159-ed2af80c-0c6c-4e0a-87a8-453d74446a1a.png)

## 3 下载 PicGo

进入<https://github.com/Molunerfinn/PicGo>，点击右边的发行版。

![图片](https://user-images.githubusercontent.com/85382878/185344930-3c42b169-1e25-4213-b254-bee3b2e76c28.png)

向下滚动，在 Assets 处选择所需的版本。

![图片](https://user-images.githubusercontent.com/85382878/185345094-5a68e4f5-b0d7-4215-a284-62052fbce93e.png)

下载。提供 PicGo-Setup-2.3.0-x64.exe 的 cdn 加速：<https://gh.con.sh/https://github.com/Molunerfinn/PicGo/releases/download/v2.3.0/PicGo-Setup-2.3.0-x64.exe>。

运行，安装，启动。

## 4 配置 PicGo

依次点击 图床设置 GitHub图床。

![图片](https://user-images.githubusercontent.com/85382878/185346225-65ce0f3a-24c6-49ca-bd56-2d68cffa9556.png)

![图片](https://user-images.githubusercontent.com/85382878/185352064-5eb5eeed-459e-48a5-ba4e-0c0fe3d7144e.png)

仓库名填写 _path_。  
分支名填写 `main`。  
Token填写 _token_。  
存储路径填写 `<文件夹名>/`，建议填写 `img/`。

自定义域名可写可不写，如果填写就会使用 cdn 进行加速。推荐填写：`https://gcore.jsdelivr.net/gh/<path>@main`。

点击 确定，推荐点击 设为默认图床。

## 5 使用方法

PicGo 会在盛传完成后自动复制图片 URL 到剪切板。

1. 把图片拖拽至上传区的方框内。
2. 点击方框，选择图片。
3. 点击快捷上传的 剪切板图片 快速上传剪切板内的图片。可以使用快捷键替代，默认是 `Cmd/Ctrl + Shift + P`。可在 PicGo 设置 中更改。
4. 点击窗口关闭键左侧的![图片](https://user-images.githubusercontent.com/85382878/185349867-3e37a820-3601-439a-a0f0-eb70e5be39de.png)，打开悬浮窗。把图片拖拽至悬浮窗内。

# 好的就到这里了。都会用了吧？

###### 2022年8月18日16点36分




