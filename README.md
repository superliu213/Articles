GitHub MarkDown语法与实例
=
##标题
1. 大标题<br>
   文本下面加上等于号 = ，那么上方的文本就变成了大标题，等号个数大于0个
2. 中标题<br>
   文本下面加上下划线-，那么上方的文本就变成了中标题，下划线个数大于0个
3. 等级表示法<br>
   一级标题前面有一个#，二级标题前面有两个#，依次类推，有六个等级 
大标题
=
中标题
-

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
##显示文本
1.普通文本
  直接输入的文字就是普通文本，换行使用\<br><br>
2.单行文本
  使用两个Tab<br>
>Hello World！<br>
3.多行文本
  在每行行首加两个Tab
>Hello World!
>MarkDown

Visit https://github.com

| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        |

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |

| Command | Description |
| --- | --- |
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |


| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

```
function test() {
  console.log("notice the blank line before this function?");
}
```

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
