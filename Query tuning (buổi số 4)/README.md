# Nguyễn Đức Lương

# Câu Hỏi
1. Với UNION sẽ có thêm Sort và Unique nên sẽ tốn nhiều cost hơn. Còn với UNION ALL thì chỉ Append nên tốn ít cost hơn.


2.
explain analyze
select s2.order_id from sales_history2 s2 EXCEPT select s.order_id from sales_history s


3.
explain analyze
select c.customer_name,c.customer_id,c.customer_tel
from customer c
inner join sales_history s on c.customer_id=s.customer_id


4.
explain analyze
select s.product_id,s.customer_id,s.order_id
from sales_history s
inner join customer c on c.customer_id=s.customer_id


5. sl bản ghi lớn hơn 20% thì không dùng index
- sl bản ghi < 0.5%  thì dùng index
- table không cần update thường xuyên


6.
- Where dùng khi đặt điều kiện trực tiếp trên trường của bảng vật lý nhưng không thể thay thế HAVING trong trường hợp điều kiện trên Group



# Câu 1
1. Viết lại câu sql sử dụng inner join

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/1c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/1m.png)

# Câu 2
1. Sử dụng Group By thay cho DISTINCT 

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/2c.png)
																											   
3. Mới                                                                                                         
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/2m.png)

# Câu 3
1. Viết lại câu sql sử dụng inner join, bỏ DISTINCT 

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/3c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/3m.png)

# Câu 4
1. Viết lại câu sql sử dụng inner join, bỏ DISTINCT , bỏ HAVING thay bằng where

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/4c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/4m.png)

# Câu 5
1. Viết lại câu sql sử dụng inner join, bỏ DISTINCT , bỏ HAVING thay bằng where

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/5c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/5m.png)

# Câu 6
1. Viết lại câu sql bỏ INTERSECT hợp lại điều kiện where

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/6c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/6m.png)

# Câu 7
1. Viết lại câu sql bỏ exists vì không cần thiết

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/7c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/7m.png)

# Câu 8
1. Viết lại câu sql bỏ NOT IN vì không cần thiết

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/8c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/8m.png)

# Câu 9
1. Viết lại câu sql bỏ DISTINCT thêm as

2. Cũ
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/9c.png)

3. Mới
![alt text](https://github.com/chalkybug/SQL-Tunning/blob/master/Query%20tuning%20(bu%E1%BB%95i%20s%E1%BB%91%204)/9m.png)









