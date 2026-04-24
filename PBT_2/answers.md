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


