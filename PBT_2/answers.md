Phần A: 
    Câu A1: 10 input types khác nhau trong HTML5, cho mỗi type:
       1. type="email" → Ô nhập text, kiểm tra có @ → Dùng đăng ký tài khoản.
       2. type="password" → Ô nhập ẩn ký tự → Dùng đăng nhập.
       3. type="number" → Ô nhập số, có tăng giảm → Dùng nhập số lượng mua.
       4. type="tel" → Ô nhập số điện thoại → Dùng thông tin giao hàng.
       5. type="url" → Ô nhập link, kiểm tra URL → Dùng nhập website.
       6. type="search" → Ô tìm kiếm → Dùng tìm sản phẩm.
       7. type="date" → Chọn ngày → Dùng chọn ngày giao hàng.
       8. type="time" → Chọn giờ → Dùng chọn giờ nhận hàng.
       9. type="checkbox" → Ô tích nhiều lựa chọn → Dùng đồng ý điều khoản.
       10. type="radio" → Chọn 1 trong nhiều mục → Dùng chọn thanh toán.
    Câu A2:
       TH1: Không submit được vì required bắt buộc phải điền, không được để trống
       TH2: Không submit đc vì type="email" bắt buộc phải có ký tự @ và tên miền
       TH3: Không submit đc vì value="15" lớn hơn giới hạn tối đa max="10"
       TH4: Không submit đc vì pattern="[0-9]{10}" bắt buộc nhập đúng 10 chữ số.
       TH5: Không submit đc vì minlength="8" bắt buộc tối thiểu 8 ký tự, nhưng user mới nhập 3 ký tự.
    Câu A3:
       3.1: Vì sao <label for="email"> quan trọng?
            Vì <label for="email"> giúp screen reader đọc tên của ô nhập liệu. Khi người dùng di chuyển đến ô email, thiết bị sẽ đọc “Email, ô nhập”. Nếu không có label, người dùng chỉ nghe “edit text” nên không biết phải nhập gì. 
        3.2: Khi nào dùng <fieldset> + <legend>?
            Khi có nhiều input cùng một nhóm nội dung. fieldset để gom nhóm, legend là tiêu đề nhóm. Điều này giúp screen reader hiểu các trường liên quan với nhau.

            Ví dụ: nhóm chọn phương thức thanh toán.
        3.3: aria-label dùng khi nào?
             Dùng khi phần tử không có text hiển thị để mô tả, ví dụ nút chỉ có icon kính lúp.
        Vì sao không nên dùng khi đã có <label>?
             Vì <label> là semantic HTML chuẩn, dễ hỗ trợ tốt hơn và hiển thị được cho cả người nhìn thấy lẫn screen reader. Nếu đã có label mà thêm aria-label, có thể gây trùng lặp hoặc xung đột tên đọc.
    Câu A4:
        4.1: loading="lazy" trên <img> là gì?
            Là chế độ tải ảnh khi ảnh gần xuất hiện trong màn hình, không tải ngay từ đầu.
        Cải thiện:
            Tăng tốc độ tải trang
            Giảm dung lượng mạng
            Tăng hiệu năng trên mobile
        Không nên dùng khi:
            Ảnh đầu trang  (hero/banner)
            Logo quan trọng hiển thị ngay
            Ảnh cần xuất hiện tức thì
        4.2:Vì sao nên có nhiều <source> trong <video>?
            Vì mỗi trình duyệt hỗ trợ codec khác nhau. Nhiều <source> giúp video chạy trên nhiều trình duyệt và thiết bị hơn.
        Ba format video web phổ biến:MP4, WebM, OGG
        4.3:alt trên <img> dùng để làm gì?
            Mô tả ảnh khi ảnh lỗi hoặc cho screen reader.
         Ví dụ alt tốt:
            Ảnh sản phẩm iPhone 16: alt="Điện thoại iPhone 16 màu đen nhìn từ mặt trước"
            Ảnh trang trí: alt=""
            Ảnh biểu đồ doanh thu Q1/2026: alt="Biểu đồ doanh thu quý 1 năm 2026 tăng dần từ tháng 1 đến tháng 3"
    Câu A5:
         Cách 1: Chỉ dùng <img> + alt: Dùng khi ảnh chỉ minh họa đơn giản, không cần chú thích hiển thị riêng.
            VD: 1. Logo thương hiệu ở đầu trang.
                2. Ảnh icon sản phẩm nhỏ trong danh sách giỏ hàng.
        Cách 2: : Dùng <figure> + <figcaption>: Dùng khi ảnh cần chú thích, mô tả.
            VD: 1. Trang chi tiết sản phẩm điện thoại.
                2. Bài viết review laptop có ảnh minh họa.


Phần C: PHÂN TÍCH & SUY LUẬN 
    Câu C1: Debug Form
         Lỗi 1: Dòng 2 — Input "Tên" không có <label for="...">, vi phạm accessibility.
Sửa: <label for="name">Tên:</label> <input type="text" id="name" name="name" required>

         Lỗi 2: Dòng 4 — Input email chỉ dùng placeholder, không có label.
Sửa: <label for="email">Email:</label> <input type="email" id="email" name="email" required>

         Lỗi 3: Dòng 6 — Input mật khẩu không có label.
Sửa: <label for="password">Mật khẩu:</label> <input type="password" id="password" name="password" required minlength="8">

        Lỗi 4: Dòng 7 — Input nhập lại mật khẩu không có label.
Sửa: <label for="confirm">Nhập lại mật khẩu:</label> <input type="password" id="confirm" name="confirm" required>

        Lỗi 5: Dòng 9 — Phone dùng type="text" thay vì type="tel".
Sửa: <label for="phone">Phone:</label> <input type="tel" id="phone" name="phone" pattern="[0-9]{10}">

         Lỗi 6: Dòng 9 — Phone dùng value="0901234567" làm dữ liệu mặc định không hợp lý.
Sửa: <input type="tel" id="phone" name="phone" placeholder="0901234567">

         Lỗi 7: Dòng 11 — <select> không có label.
Sửa: <label for="city">Thành phố:</label> <select id="city" name="city">...</select>

        Lỗi 8: Dòng 16 — Label điều khoản không gắn với checkbox, không thể click chọn.
Sửa: <input type="checkbox" id="agree" name="agree" required> <label for="agree">Tôi đồng ý điều khoản</label>
     Câu C2: 
        2.1: CMND/CCCD (12 chữ số): pattern="[0-9]{12}"
             Số tài khoản (10-15 chữ số): pattern="[0-9]{10,15}"
        2.2: HTML5 Validation không đủ an toàn cho ngân hàng vì HTML5 chạy ở Frontend (trên máy user),có thể dùng F12 xóa thuộc tính required hoặc pattern trong HTML là có thể gửi bất cứ thứ gì lên.
        2.3:Ba loại validation HTML5 không thể làm được (cần JavaScript)
             1. Kiểm tra PIN nhập lại có trùng PIN ban đầu hay không.
             2. Kiểm tra CMND/CCCD đã tồn tại trong hệ thống chưa.
             3. Kiểm tra số tài khoản có hợp lệ theo ngân hàng hoặc tồn tại thật không.
        2.4: Hai rủi ro bảo mật nếu chỉ validate trên Frontend mà không validate Backend
             1. Kẻ xấu bypass validation bằng cách gửi dữ liệu giả trực tiếp lên server.
             2. Dữ liệu rác hoặc sai định dạng được lưu vào database, gây lỗi hệ thống hoặc gian lận.