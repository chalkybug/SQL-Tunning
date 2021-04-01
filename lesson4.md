# lesson 4

1. select cần gì thì select nấy
2. alias khi select 2 bảng
3. where và having
  - having fetch hết về rồi mới lọc
  - where lọc về rồi mới fetch

4. Hints: không hỗ trợ trên posgress

## Cải tiến hiệu năng
1. Sử dụng union all thay cho union
2. Sử dụng union thay vì or: postgress tự hiểu còn oracle thì không
3. So sánh exist và in
  - Chọn `IN` khi inner query nhỏ
  - Còn chọn `EXISTS` khi outer query lớn

[outer query] là như kiểu
[inner query] là câu query ở trong cầu lệnh

4. khi nào thì đánh index
  - sl bản ghi lớn hơn 20% thì không dùng index
  - sl bản ghi < 0.5%  thì dùng index
  - table không cần update thường xuyên
