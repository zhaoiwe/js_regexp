# js_regexp
js正则表达式

。g:global全文搜索，不添加搜索到第一个匹配停止
。i：忽略大小写，默认情况大小写敏感
。m：多行搜索
>>replace(reg,x) js根据指定的正则表达式替换
   例 "a1b2c3d4".replace(/[1234]/g,"5");
   结果 a5b5c5d5
   <br>
*  []  一般情况下正则表达式一个字符对应字符串一个字符 可以使用元字符[]来构建一个简单的类，所谓类是指符合某些特征的对象，一个泛指，而不是特指某个字符
    表达式[abc]：把字符 a 或 b 或 c 归为一类，表达式可以匹配这类的字符，即匹配abc中的一个
* ^ 取反 例[^ab]匹配不是字符ab的字符
    "abc23de22".replace(/[^ab]/g,"x") 结果 abx23xx22
 * 范围类
     [A-Z] 大写a-z全部[A-Za-z]包括大写小写的字母
     [0-9] 匹配0-9全部数字 例  19999-002-233.replace(/[0-9]/g,"x") 结果xxxxx-xxx-xxxx
     </br>
     [0-9-]匹配0-9及- 例 19990-000-333.replace(/[0-9-]/g,"x") 结果xxxxxxxxxxx
     <br>
 * 预定义类<br>
  正则表达式提供了 预定义类 匹配常见的字符类<br>
    .  等价于 [^\r\n] 表示除了回车符和换行符之外的所有的字符<br>
    \d 等价于 [0-9] 数字字符<br>
    \D 等价于 [^0-9] 非数字字符<br>
    \s 等价于 [\t\n\x0B\f\r] 空白符 s:space<br>
    \S 等价于 [^\t\n\x0B\f\r] 非空白符<br>
    \w 等价于 [a-zA-Z_0-9] 单词字符（字母、数字下划线） w:word<br>
    \W 等价于 [^a-zA-Z_0-9] 非单词字符
    提示：大写的表示取反<br>
     例子：<br>
    匹配一个 ab+数字+任意字符 的字符串<br>
    使用范围类：ab[0-9][^\r\n]    使用预定义类：ab\d.<br>
常见的边界匹配字符：<br>
    ^ 以XXX开始<br>
    $ 以XXX结束<br>
    \b 单词边界<br><br>
    \B非单词边界<br>
  例子：<br>
   1. '@123@abc@'.replace(/^@./g,'Q');<br><br>
      "Q23@abc@"<br>
   2.'@123@abc@'.replace(/.@$/g,'Q');<br>
     "@123@abQ"<br>
   3.'@123@abc@'.replace(/.@/g,'Q');<br>
     "@12QabQ"<br>
* m,多行处理。加上m,告诉它把换行符当做新行处理。<br>
* {}:量词
*（）:分组
