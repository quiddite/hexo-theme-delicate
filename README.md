# hexo-theme-delicate

> 依据bootstrap设计的一款hexo主题  
> [Demo site](https://kartjim.top/delicate)

<div style="display:flex;justify-content: space-evenly;">
<a href="https://nodejs.org"><img src="https://img.shields.io/badge/node-%3E%3D10.9.0-blue"></a>
<a href="https://hexo.io"><img src="https://img.shields.io/badge/hexo-4.3.0-brightgreen"></a>
<a href="https://github.com/can-dy-jack/hexo-theme-delicate/blob/master/LICENSE"><img src="https://img.shields.io/badge/license-MIT-orange"></a>
</div>

## 教程

使用主题默认您已创建过[hexo](https://hexo.io)项目

### 下载

1. npm

```bash
npm i hexo-theme-delicate
```

然后去 `node_modules` 文件夹找到 `hexo-theme-delicate` 文件夹，将其剪切到目录下的 `themes` 文件夹下。

2. git

```git
git clone https://github.com/can-dy-jack/hexo-theme-delicate.git theme/delicate
```

3. 或者你可以**下载本仓库的代码，解压到theme文件夹之下，重命名文件夹为`delicate`。**

### 使用

之后只需更改配置 `_config.yml`：

```yml
theme: delicate
```

### 本主题自定义 front-matter

1. 置顶文章

在文章的Front-matter添加: `top: true`即可置顶文章

```yml
top: true
```

3. 开启MathJax
```yml
mathjax: true
```
**文章没有公式请不要添加，会影响页面加载速度。**

### 本主题内置tag

1. note

```ejs
{% note [class] %}
note-info
{% endnote %}
```

效果：
![image.png](https://s2.loli.net/2021/12/11/d74VfQNhG9ELW1P.png)

2. color

> 用于设定文字颜色
> 文字颜色可以随便设置，颜色名称 | HEX | rgb() | rgba() | HSL() 等等均可。
> 需要注意的是，前面的颜色值和后面的文字中间如果有空格，需要加上引号。

```ejs
{% color [color] 文字 %}
```

3. alert

> 基于Bootstrap的alert

使用：

```ejs
{% alert [class] %}
A simple primary alert—check it out!
{% endalert %}
```

可选值：

- primary
- secondary
- success
- danger
- warning
- info
- light
- dark

4. collapse

> bootstrap collapse

```ejs
{% collapse [class] [按钮文字] [id] %}
折叠内容
{% endcollapse %}
```

color red 三个参数均不可少

|参数|注意事项|
|:---:|:---|
|[class]|按钮的样式，选项为[boostrap的按钮样式](https://v4.bootcss.com/docs/components/buttons/)|
|[按钮文字]|按钮上面显示的文字|
|[id]|在同一篇文章里，每个collapse的id需要唯一，即每个collapse的id需要设定不同的值；值随意，不同就行。|

例子：

```ejs
{% collapse info '点击显示折叠内容' id1 %}
这里写需要隐藏的文字。
{% endcollapse %}
```

5. toasts


例子：
```markdown
{% toasts tip 提示 %}
**Markdown** is supported, Text can be bold, italic, or strikethrough. 
Links should be blue with no underlinesinline codeinline code inside link
{% endtoasts %}
```
效果：

![b71Rxg.png](https://s1.ax1x.com/2022/03/12/b71Rxg.png)

可选值：

- tip
- note
- danger
- warning

More details Read：[kartjim.cn/delicate](https://kartjim.cn/delicate/2021/11/12/code-test)

### markdown

[markdown样式](https://kartjim.cn/delicate/2021/11/14/markdown%E6%B5%8B%E8%AF%95%E6%96%87%E4%BB%B6/)

## 参考项目

- [stevenlei/CSS Dynamic Background](https://codepen.io/stevenlei/pen/ZEJxXGL?editors=1100)
- [juejin-全面改造属于你的个性化博客](https://juejin.cn/post/6997775533840793614#heading-5)

## 开发计划

- 404页面
- 文章分享功能
- 永久链接问题
- 优化评论系统
- 优化雪花飘落效果 + 用户选项
