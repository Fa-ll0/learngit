
# Dom:
可以访问与修改相邻的父兄节点的内容，判断类型等
## 初步了解：
## 属性：
- document.baseURI
一般返回绝对路径，但是设置后由\<base>标签决定
- document有两个子节点，docType和html根元素节点

## 方法：
- 添加节点对象，判断存在性，复制等节点操作
- 遍历用的nodelist，collection
## 正式学习：
- document节点：
(window.)document
  - 属性
  1. document.body
document.head
document.title
document.documentElement(html)
document.stylesheets(css)
  2. document.links
document.forms
document.images
document.scripts
  3. document.documentURI(继承document)
/document.URL(继承HTMLDocument)
document.domain(只有域名没有端口)
document.referrer
document.cookie
document.getElementsByTagName()(元素标签)
document.getElementsByClassName()
(css类名，多个参数用空格分隔，别忘了加‘’)
document.getElementsByName()
***document.getElementById()***返回元素节点
- Element节点(不是element这个单词)
  1. Element.id
  2. Element.tagName
  3. Element.attributes
  4. element.className/element.classList
 - Text节点代表元素节点和属性节点的文本内容
## Dom先这样。

