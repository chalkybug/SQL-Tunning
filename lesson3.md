## chữa bài tập buổi 2

select first_name, last_name from users where first_name = 'joe'

- đánh index cả vào first_name và last_name để vùng tìm kiếm chỉ để index
- only index scan


chữa câu 7;
`
select f.title, f.dex, f.rating, f.length, avg_info.length
join ( select ... form film )
`
## Luyện tập:
1. đánh index
`create index on users(first_name)`
2. viết lại câu lệnh where
`select age, email from users where first_name ='Michael' and  SUBSTR(last_name,1,3) = 'Leo'`
3. đánh index func
`create index on users(SUBSTR(first_name, 1,3))`
4. đánh index func
`create index on product(lower(color))`
5. bt
`create index on sales_history((quantity * unit_price))`
6. bt
`create index on product((list_price < standard_cost))`
7. bt
`create index  on sales_history(date_part('year', sales_date))`
8. bt
`create index  on product(list_price)`
9. đánh thêm index func
`create index  on sales_history(date_part('day', sales_date))`
10. sử lại where và đánh index age
`where age = 60`
11. bt
`create index  on users(lower(last_name))`
12. bt

13. bt
`select p1.product_id, p1.product_name, p1.weight, p2.avg_weight
from product p1
join (select product_category, avg(weight) as avg_weight
	from product product_weight group by product_category) as p2 
on p1.product_category= p2.product_category
where p1.list_price between 300 and 400`
14. bt
`create index  on users(last_name)`
15. bt
`where (standard_cost + 30) > 100  => where (standard_cost) > 70 `
16. bt
`where ( 2019 - age ) between 1990 and 2000 => where age between 19 and 29`
17. bt
`explain analyze
select p1.product_id, p1.product_name, p2.total_sale
from product p1
inner join (select product_id, sum(sale_amount) AS total_sale
   from sales_history2 group by product_id ) as p2 
  on p1.product_id =p2.product_id
`
18. bt
`explain analyze
select product.product_name , customer.customer_name
from sales_history2
join product on  product.product_id = sales_history2.product_id
join customer on customer.customer_id = sales_history2.customer_id
where sales_history2.product_id = 10
and sales_history2.customer_id = 10009
`
