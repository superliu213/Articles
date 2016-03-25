
GitHub MarkDown语法与实例
==

## 标题
1. 大标题<br>
   文本下面加上等于号 = ，那么上方的文本就变成了大标题，等号个数至少2个
2. 中标题<br>
   文本下面加上下划线-，那么上方的文本就变成了中标题，下划线个数至少2个
3. 等级表示法<br>
   一级标题前面有一个#，随后跟一个空格，二级标题前面有两个#，依次类推，有六个等级
   添加空格是因为这样比较通用
大标题
==
中标题
--

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
##显示文本
1.普通文本
  直接输入的文字就是普通文本，换行使用<br>
2.单行文本
  使用两个Tab
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

Sometimes you want numbered lists:

1. One
2. Two
3. Three

Sometimes you want bullet points:

* Start a line with a star
* Profit!

Alternatively,

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  - Like this
  - And this

If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

```javascript
if (isAwesome){
  return true
}
```

GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ] This is an incomplete item

When you include a task list in the first comment of an Issue, you will see a helpful progress bar in your list of issues. It works in Pull Requests, too!

And, of course emoji! :sparkles: :camel: :boom:

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>


[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
