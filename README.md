汇总一些工作上MYSQL知识点
===
#`我们工作中除了增删改查用得比较多的就是统计了`

>>`常用SQL`
---
`统计数据总量(`只有一个字段的时候，* 比 1快，没有主键的时候1比*快 建议任何时候都用 * `)`   
<br>
select count(*) from  table 

`统计数据总量去重`
<br>
select count(DISTINCT,'id') from table

`按指定顺序检索数据`
<br>
select * from table order by field (id,'1','2','3');

`当天只有一条数据的数据`
<br>
select * from table where day=now() group by id having count('id')=1
<br>
`获取最新十条数据`
<br>
select * from table order by id desc limit 10
>>`常用函数`
<br>
`FROM_UNIXTIME(时间戳)   时间戳转换日期`

<br>
`UNIX_TIMESTAMP(日期)  日期转换时间戳`

<br>
`NOW()       当前时间戳`
<br>
`concat(str1,str2)  将多个字符串连接(注意有一个参数是null,返回值位null)`

<br>
`concat_ws('分隔符',str1,str2)  用分隔符拼接字符串(注意分隔符为null,返回值位null)`

<br>
`group_concat()    如果与group by 搭配使用 相同的列都拼接起来 ，否则所有的列拼接`

</br>