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

Phần B:
    B3: debug-html
Lỗi 1: Dòng 1 - <!DOCTYPE> thiếu html - thêm html
Lỗi 2: Dòng 2 - html thiếu lang = "vi" - thêm lang = "vi"
Lỗi 3: Dòng 4 - Thẻ title chưa có đóng - Thêm thẻ đóng </title>
Lỗi 4: Dòng 5 - Giá trị charset sai - Sửa thành UTF-8
Lỗi 5: Dòng 8 - Thẻ đóng h1 sai 
Lỗi 6: Dòng 12 - Thẻ đóng a sai 
Lỗi 7: Dòng 20 - Thẻ  thiếu dấu "" và thiếu alt — Sửa thành Hình ảnh iPhone
Lỗi 8: Dòng 22 - Sai vị trí thẻ đóng 
Lỗi 9 Dòng 40 - Thừa 1 thẻ 
Lỗi 10: Dòng 45 - Thẻ p chưa đóng - Thêm thẻ p
Lỗi 11: Dưới dòng 47 - Thiếu thẻ đóng html - Thêm html
    B4: Phân tích trang WEB thật
       4.1:
    <header>: Phần đầu trang Chứa logo, menu, tìm kiếm
    <nav>: Thanh menu đầu trang	điều hướng đến Điện thoại, Laptop, Tablet...
    <footer>: Cuối trang thông tin công ty, hỗ trợ, chính sách
       4.2: 
       Bảng hiển thị: Hệ điều hành, chip xử lí, ram, dung lượng . Giúp người mua lựa chọn kĩ càng trước khi mua sản phẩm.
       Có dùng <Tbody>
       4.3:
       form có:
          action :    tim-kiem hoặc URL tìm kiếm nội bộ
          method :  	GET
        Input types nào được dùng:
          type="text"
          type="submit"
Phần C:
    C2:
    Ý kiến “chỉ cần dùng <div> cho mọi thứ rồi thêm class” khá tiện, nhưng không tối ưu
 về kỹ thuật. <div> chỉ là thẻ trung tính, không mang ý nghĩa nội dung. Trong khi đó, 
 semantic HTML như <header>, <nav>, <main>, <article> giúp trình duyệt và công cụ tìm kiếm
 hiểu rõ cấu trúc trang.Lý do đầu tiên là SEO. Google dựa vào cấu trúc HTML để xác định đâu 
 là nội dung chính, đâu là menu hay phần phụ. Ví dụ, một bài viết đặt trong <article> với tiêu
 đề <h1> sẽ dễ được nhận diện và lập chỉ mục tốt hơn so với việc tất cả đều là <div>. Điều này
 giúp tăng khả năng xuất hiện trên kết quả tìm kiếm.Lý do thứ hai là Accessibility. Người 
 khiếm thị dùng screen reader để truy cập web. Khi trang có <nav>, họ có thể chuyển nhanh đến
 menu; có <main> thì vào thẳng nội dung chính. Nếu chỉ toàn <div>, thiết bị hỗ trợ khó hiểu 
 bố cục, làm trải nghiệm kém hơn.Tuy nhiên, <div> vẫn phù hợp trong nhiều trường hợp như làm 
 container chia layout bằng Flexbox/Grid, nhóm phần tử để tạo hiệu ứng CSS hoặc thao tác 
 JavaScript. Vì vậy, <div> rất hữu ích, nhưng không nên thay thế hoàn toàn semantic HTML.