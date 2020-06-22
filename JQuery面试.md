## Jquery ##



### $(document).ready() 是个什么函数？为什么要用它？ ###

ready函数用于在文档进入ready状态时执行代码。当DOM完全加载，JQuery允许你执行代码。最大好处在他适应所用浏览器。而Window.onload函数还要等待大型图片，音频，视屏加载完成才执行。



###  jQuery 库中的 $() 是什么？ ###

$()函数是JQuery函数的别称，$()函数用于将任何对象包装成JQuery对象，接着你就允许调用JQuery对象上的方法了。

###如何找到所有 HTML select 标签的选中项？ ###

如<Select id='c' class="c_select" name="n_select">
    <option value="1">1<option>
    <option value="2">2<opyion>
  </select>

JS代码`
   获取所用选项中的项
   $('[name=n_select] :selected');
   $('.c_select option:selected');
   $('.c_select').find('option:selected');
  
   获取一个
   $('[name=n_select] :selected').text()
`


###jQuery 里的 each() 是什么函数？你是如何使用它的？###

each() 函数就像是 Java 里的一个 Iterator，它允许你遍历一个元素集合。你可以传一个函数给 each() 方法，被调用的 jQuery 对象会在其每个元素上执行传入的函数。有时这个问题会紧接着上面一个问题，举个例子，如何在 alert 框里显示所有选中项。我们可以用上面的选择器代码找出所有选中项，然后我们在 alert 框中用 each() 方法来一个个打印它们，代码如下：


$('[name=NameOfSelectedTag] :selected').each(function(selected) {
    alert($(selected).text());
});
