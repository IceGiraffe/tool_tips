* 插入代码片段
  * 使用命令面板的插入代码片段功能
  * 写代码时，VS Code的intellisense功能会自动提升代码片段
* 创建代码片段
  * 命令面板——用户代码片段——管理
  * 创建新的代码片段，可以选择全局片段或者当前工作区生效的局部片段，也可以针对某种语言创建代码片段，该片段只有特定语言下生效
* 代码片段的生效范围
  * 语言维度：
    * 针对某种语言创建代码片段之后，相关配置信息会保存在`language-name.json`文件中，如`cpp.json`。
    * 多语言片段会保存在`snippet-name.code-snippets`中，在全局片段的scope字段中，也可以指定该片段的生效语言。
  * 项目维度：
    * 当前项目生效的片段存放在当前文件夹`.vscode`文件夹下的`.code-snippets`结尾的JSON文件中。
* 代码片段的用法
  * Tabstops：使用Tab可以在`$1,$2,$3...`依次遍历；
  * 占位符是包含默认值的Tabstops，如`${1:foo}`；
  * 占位符支持嵌套`${1:another${2:placeholder}}`
  * 占位符支持选择，用管道字符包围逗号隔开的若干个选择即可`${1|one,two,three|}`
* Snippet还支持一些全局变量，比如当前时间等，使用时用`$NAME`即可。