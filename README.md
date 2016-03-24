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
>Hello World！

3.多行文本
  在每行行首加两个Tab
>Hello World!<br>
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

**This is bold text**

*This text is italicized*

~~This was mistaken text~~

**This text is _extremely_ important**

Use `git status` to list all new or modified files that haven't yet been committed.

Some basic Git commands are:
```
git status
git add
git commit
```

This site was built using [GitHub Pages](https://pages.github.com/).

- George Washington
- John Adams
- Thomas Jefferson

1. James Madison
2. James Monroe
3. John Quincy Adams

1. Make my changes
  1. Fix bug
  2. Improve formatting
    * Make the headings bigger
2. Push my commits to GitHub
3. Open a pull request
  * Describe my changes
  * Mention all the members of my team
    * Ask for feedback


- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request

@github/support What do you think about these updates?

@octocat :+1: This PR looks great - it's ready to merge! :shipit:

Let's rename \*our-new-project\* to \*our-old-project\*.
