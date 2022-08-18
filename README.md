# 手把手教你用 GitHub 自建私人图床

参考文章：[使用Github+picGo搭建图床，保姆级教程来了](https://zhuanlan.zhihu.com/p/489236769 "知乎")

## 0 准备工作

一台电脑，一个 GitHub 账号，一个人。

## 1 资源准备

打开 GitHub，网址：<https://github.com/>。登录（或许要先注册）。

### 仓库搭建

在屏幕右上角点击加号，在下拉菜单中点击 New repository，也可以直接去<https://github.com/new>。

![图片](https://user-images.githubusercontent.com/85382878/185338583-ac38d05c-7bc5-436e-9e66-6adb47748c57.png)

在页面中上面一个红色方框所示的位置填写仓库名称，不要用中文。在右边显示勾勾的时候就可以了。建议勾选复选框，添加 README.md 文件，内容自动生成，可以更改。

![图片](https://user-images.githubusercontent.com/85382878/185338957-6b0dc1cd-81e4-4807-867d-369849f4cb8b.png)

如果你填入空格之类的东西，会弹出黄色方框，加粗内容表示最终仓库名称。

![图片](https://user-images.githubusercontent.com/85382878/185340002-9286bb8a-e7e2-442b-8566-bd8980950e6b.png)

**注意** 起名的时候要让仓库名尽量的短，因为这会直接出现在最终的图片 URL 中。

滚动到最底部，点击绿色按钮即可。耐心等待。

![图片](https://user-images.githubusercontent.com/85382878/185340479-af421674-281f-44b5-bb06-bd78ef18d935.png)

### 令牌生成

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

复制红色框框所标识的文本。妥善保存，这很重要，以后还会用到。我们暂且把他叫做 _token_。刷新页面就看不到了。

![图片](https://user-images.githubusercontent.com/85382878/185344159-ed2af80c-0c6c-4e0a-87a8-453d74446a1a.png)

### 下载 picGo

进入<https://github.com/Molunerfinn/PicGo>，点击右面的发行版。

![图片](https://user-images.githubusercontent.com/85382878/185344930-3c42b169-1e25-4213-b254-bee3b2e76c28.png)

向下滚动，在 Assets 处选择所需的版本。

![图片](https://user-images.githubusercontent.com/85382878/185345094-5a68e4f5-b0d7-4215-a284-62052fbce93e.png)

下载。提供 PicGo-Setup-2.3.0-x64.exe 的 cdn 加速：<https://gh.con.sh/https://github.com/Molunerfinn/PicGo/releases/download/v2.3.0/PicGo-Setup-2.3.0-x64.exe>。



