# Tale 指南（Tale Guideline）

修改自：https://github.com/mattcone/markdown-guide
Modified after: https://github.com/mattcone/markdown-guide

## 总览

这个 Tale 语法指南，提供了所有 Tale语法元素的快速概述。

This Tale Guideline provides a quick overview of all the Tale syntax elements.

## Tale 支持的 Markdown 语法

Tale 是一个基于 Markdown 修改的语言，Tale 原生支持大部分基础 Markdown 语法。

<table class="table table-bordered">
  <thead class="thead-light">
    <tr>
      <th>元素</th>
      <th>Markdown 语法</th>
      <th>正则式</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/markdown-cn/#headings">标题</a></td>
      <td><code># 一级标题（H1）<br>
                ## 二级标题（H2）<br>
                ### 三级标题（H3）</code></td>
                <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#bold">粗体</a></td>
      <td><code>**粗体 文本**</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#italic">斜体</a></td>
      <td><code>*斜体 文本*</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#blockquotes-1">块引用</a></td>
      <td><code>> 块引用</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#ordered-lists">有序列表</a></td>
      <td><code>
        1. 第一个物品<br>
        2. 第二个物品<br>
        3. 第三个物品<br>
      </code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#unordered-lists">无序列表</a></td>
      <td>
        <code>
          - 第一个物品<br>
          - 第二个物品<br>
          - 第三个物品<br>
        </code>
      </td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#code">代码</a></td>
      <td><code>`代码`</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#horizontal-rules">分隔线</a></td>
      <td><code>---</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#links">链接</a></td>
      <td><code>[标题](https://www.example.com)</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#images-1">图片</a></td>
      <td><code>![文本](图片.jpg)</code></td>
      <td>N/A</td>
    </tr>
  </tbody>
</table>

<table class="table table-bordered">
  <thead class="thead-light">
    <tr>
      <th>Element</th>
      <th>Markdown Syntax</th>
      <th>Regex</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/markdown-cn/#headings">Heading</a></td>
      <td><code># H1<br>
          ## H2<br>
          ### H3</code></td>
          <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#bold">Bold</a></td>
      <td><code>**bold text**</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#italic">Italic</a></td>
      <td><code>*italicized text*</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#blockquotes-1">Blockquote</a></td>
      <td><code>> blockquote</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#ordered-lists">Ordered List</a></td>
      <td><code>
        1. First item<br>
        2. Second item<br>
        3. Third item<br>
      </code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#unordered-lists">Unordered List</a></td>
      <td>
        <code>
          - First item<br>
          - Second item<br>
          - Third item<br>
        </code>
      </td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#code">Code</a></td>
      <td><code>`code`</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#horizontal-rules">Horizontal Rule</a></td>
      <td><code>---</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#links">Link</a></td>
      <td><code>[title](https://www.example.com)</code></td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="/markdown-cn/#images-1">Image</a></td>
      <td><code>![alt text](image.jpg)</code></td>
      <td>N/A</td>
    </tr>
  </tbody>
</table>

## Tale 语法

以下为 Tale 特有的语法，其他 Markdown 编辑器或许不支持这些语法。

<table class="table table-bordered">
  <thead class="thead-light">
    <tr>
      <th>元素</th>
      <th>Tale 语法</th>
      <th>正则式</th>
      <th>注释</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/tale-cn/#jump">跳转</a></td>
      <td><code>
          <文字>(识别符)
      </code></td>
      <td><code>\(.+\)<.+></code></td>
      <td>识别符用来确认跳转位置</td>
    </tr>
    <tr>
      <td><a href="/tale-cn/#dialougue">角色对白</a></td>
      <td><pre><code>    角色名称:</code></pre></td>
      <td><code>\t.+:<.+></code></td>
      <td>语法为 tab + 角色名 + : </td>
    </tr>
    <tr>
    <td><a href="/tale-cn/#dialougue">修饰表</a></td>
    <td>
<pre><code>'''
example_config = True
'''</code></pre>
    </td>
    <td>N/A</td>
    <td>用以修饰配置</td>
    </tr>
  </tbody>
</table>

<table class="table table-bordered">
  <thead class="thead-light">
    <tr>
      <th>Element</th>
      <th>Tale Syntax</th>
      <th>Regex</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/tale-cn/#jump">Jump</a></td>
      <td><code>
          <Text>(ID)
      </code></td>
      <td><code>\(.+\)<.+></code></td>
      <td>use ID locate the position for Jump</td>
    </tr>
    <tr>
      <td><a href="/tale-cn/#dialougue">Dialougue</a></td>
      <td><pre><code>    Name:</code></pre></td>
      <td><code>\t.+:<.+></code></td>
      <td> tab + Name + : </td>
    </tr>
    <tr>
    <td><a href="/tale-cn/#dialougue">Modifiers</a></td>
    <td>
<pre><code>'''
example_config = True
'''</code></pre>
    </td>
    <td>N/A</td>
    <td>Use modifier to override configuration.</td>
    </tr>
  </tbody>
</table>
