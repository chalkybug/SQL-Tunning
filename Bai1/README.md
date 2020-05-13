# Câu 1
1. Số lượng các node : 2
2. Thông tin chi tiết của từng node: Cost, rows, width
- Seq Scan: (cost=0.00..69.00 rows=43 width=174)
- Sort : cost=70.17..70.27 rows=43 width=174
3. Node nào được chạy đầu tiên
- Seq Scan
4. Trình tự thực hiện các node
- Seq Scan => Sort
	
5. ![alt text](https://images.pexels.com/photos/1030982/pexels-photo-1030982.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500)

# Câu 2
1. Số lượng các node : 3
2. Thông tin chi tiết của từng node: Cost, rows, width
- Seq Scan (cost=0.00..66.50 rows=191 width=6)
- HashAggregate  (cost=67.46..67.52 rows=5 width=36)
- Sort  (cost=67.58..67.59 rows=5 width=36)
3. Node nào được chạy đầu tiên
- Seq Scan
4. Trình tự thực hiện các node
- Seq Scan => HashAggregate => Sort
	
5. ![alt text](https://images.pexels.com/photos/1030982/pexels-photo-1030982.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500)

# Câu 3
1. Số lượng các node : 3
2. Thông tin chi tiết của từng node: Cost, rows, width
- Seq Scan on film  (cost=0.00..66.50 rows=191 width=6)
- HashAggregate  (cost=67.93..68.02 rows=2 width=36)
- Sort  (cost=68.03..68.04 rows=2 width=36)
3. Node nào được chạy đầu tiên
- Seq Scan
4. Trình tự thực hiện các node
- Seq Scan => HashAggregate => Sort
	
5. ![alt text](https://images.pexels.com/photos/1030982/pexels-photo-1030982.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500)

# Câu 4
1. Số lượng các node : 5
2. Thông tin chi tiết của từng node: Cost, rows, width
- Seq Scan on language  (cost=0.00..1.06 rows=6 width=88)
- Hash  (cost=1.06..1.06 rows=6 width=88)
- Seq Scan on film  (cost=0.00..66.50 rows=418 width=21)
- Hash Join  (cost=1.14..69.51 rows=418 width=103)
- Sort  (cost=87.71..88.75 rows=418 width=103)
3. Node nào được chạy đầu tiên
- Seq Scan on language
4. Trình tự thực hiện các node
- Seq Scan on language => Seq Scan on film => Hash =>  Hash Join => Sort
	
5. ![alt text](https://images.pexels.com/photos/1030982/pexels-photo-1030982.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500)


# Câu 5
1. Số lượng các node : 6
2. Thông tin chi tiết của từng node: Cost, rows, width
- Seq Scan on language  (cost=0.00..1.06 rows=6 width=88)
- Hash  (cost=1.06..1.06 rows=6 width=88)
- Seq Scan on film  (cost=0.00..66.50 rows=418 width=4)
- Hash Join  (cost=1.14..69.51 rows=418 width=86)
- HashAggregate  (cost=71.60..71.68 rows=6 width=116)
- Sort  (cost=71.75..71.77 rows=6 width=116)
3. Node nào được chạy đầu tiên
- Seq Scan on language
4. Trình tự thực hiện các node
- Seq Scan on language => Seq Scan on film => Hash =>  Hash Join => HashAggregate => Sort
	
5. ![alt text](https://images.pexels.com/photos/1030982/pexels-photo-1030982.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500)
