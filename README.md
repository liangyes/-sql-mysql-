汇总一些工作上MYSQL知识点
===
#我们工作中除了增删改查用得比较多的就是统计了
##常用SQL
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

`只有一条数据的数据`
<br>
select * from table group by id having count('id')=1