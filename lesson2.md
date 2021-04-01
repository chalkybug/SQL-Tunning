# lesson2
chữa bài câu số 6: tại sao subquery lấy ra một trường nhưng trong câu lệnh explain analyze lại trả về 2 trường output
=> vì phải lấy thêm trường so sánh trong câu lệnh where


Câu hỏi:
1. sự khác nhau giữa hash jnner join và nested inner join


Bài mới:
- có 2 cách đọc dữa liệu từ bảng

Câu hỏi:
- 1 row lớn hơn 8kb thì sao


sự khác nhau giữa SQL_Server và Posgress là trong posgress chỉ có none-cluter nên có 2 vùng là index và heap
còn trong SQL_Server thì gộp lại nên có thêm index cluter

2. Index only scan
- Chỉ lấy ở phần index nên sẽ nhanh hơn

3. Bitmap scan
- seq scan + index scan
- tạo thêm 1 phần bitmap để tránh việc di chuyển qua lại nhiều lần giữa index và heap
- lúc explain thì có phần recheck condition
- có thêm một trường hợp hay dùng bitmap scan: trong câu lệnh có 2 điều where đều được đánh index
