# js_regexp
js正则表达式

。g:global全文搜索，不添加搜索到第一个匹配停止
。i：忽略大小写，默认情况大小写敏感
。m：多行搜索
>>replace(reg,x) js根据指定的正则表达式替换
   例 "a1b2c3d4".replace(/[1234]/g,"5");
   结果 a5b5c5d5
