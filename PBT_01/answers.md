Câu A1: HTTP & Browser
1. Khi bạn gõ https://shopee.vn vào trình duyệt và nhấn Enter, hãy liệt kê đúng thứ tự ít nhất 5 bước xảy ra (từ DNS lookup đến render).(Nguồn từ Hành trình 0.3s xuyên đại dương)
    1 Request  xuất phát từ laptop->trình duyệt bắt đầu tìm ra IP của shoppe dựa vào DNS
     → đi qua router WiFi nhà trọ
    2→ Qua nhà mạng VNPT → chạy xuyên cáp quang dưới đáy Thái Bình Dương
    3→ Đến data center của Shoppe ở Hà Nội
    4→ Server xử lý: "Minh muốn xem áo phông"
    5→ Response chạy ngược lại: cáp quang → VNPT → router → laptop
    6→ Chrome nhận file HTML, CSS, JS → render ra giao diện → Minh thấy mẫu áo phông
2. Tab Network trong DevTools cho biết WEB tải những gì.(Mục 4.3 chương một)
Câu A2: Semantic HTML
   Lỗi phần đầu trang: Dùng <div class="header"> thay vì thẻ chuẩn <header>
   Lỗi vùng nội dung chính: Dùng <div class="main"> thay vì dùng thẻ <main>
   Lỗi khối nội dung sản phẩm: Dùng <div class="product"> thay vì thẻ <article>
   Lỗi phần chân trang: Dùng <div class="footer"> thay vì dùng thẻ <footer>
Câu A3: Block vs Inline
  Không chạy code, hãy vẽ tay (hoặc mô tả bằng text art) kết quả hiển thị của đoạn HTML đã cho là:
      Hộp 1
      Text A Text B
      Hộp 2
      Text C Text D
      Hộp 3
  Vì:
    Hộp 1: Đây là phần tử block nó sẽ luôn bắt đầu từ dòng mới và chiếu chiều rộng nhiều nhất có thể.
    Text A Text B: Đây là phần tử inline không xuống dòng mà chỉ chiếm đủ độ rộng.
    Hộp 2 : Xuống dòng riêng.
    Text C Text D: (Boi dam) vì thẻ strong có mang tính chất quan trong.
    Hộp 3 : Xuống dòng riêng.
Câu A4: Table
<thead>: Chứa phần tiêu đề của bảng, thường là đầu bảng.
<tbody>: Chứa nội dung chính của bảng, giữa bảng.
<tfoot>: Chứa phần cuối bảng, thường dùng tổng kết.
 KHÔNG NÊN dùng table để tạo layout trang web vì:
     1. HTML5 cung cấp các thẻ để xây dựng bố ccuj nếu sử dụng table thì sẽ phá vơ đi tiêu chuẩn 
     2. Khó tương thích tương thích với điện thoại dó các thẻ trong table vô cùng cứng ngắt
     3. Nếu như table phức tạp sẽ tốn nhiều thời gian tải trang hơn
     4. Khó co giãn trên điện thoại hoặc màn hình nhỏ, dễ bị tràn nội dung
