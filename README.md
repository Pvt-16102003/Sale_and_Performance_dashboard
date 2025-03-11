# Sale_and_Performance_dashboard
## Tổng quan dự án
Dự án Dashboard cung cấp cho Olist Store cái nhìn tổng quan hơn về tình hình kinh doanh, nắm bắt chính các dữ kiện kinh doanh theo thời gian cũng như các thành phần tác động, đi sâu vào quan sát các yếu tố ảnh hưởng đến sale và chất lượng của việc giao hàng
- Nắm bắt nhanh chóng các ngành hàng, mặt hàng và vị trí hoạt động kinh doanh
- Làm rõ các yếu tố ảnh hưởng lớn đến hiệu suất
- Tối ưu hóa quy trình mua sắm
- Hỗ trợ điều tra và giảm các loại chi phí trong quá trình bán hàng
- Cải thiện hiệu quả hoạt động chung

## Một số tính năng chính của Dashboard
- Thông tin chi tiết dựa trên dữ liệu
- Số liệu có thể tùy chỉnh theo nhiều chiều
- Giao diện thân thiện với người dùng

## Công cụ và nguồn dữ liệu
- Công cụ: Tableau, Python
- Nguồn dữ liệu: Kaggle (Bộ dữ liệu này bao gồm các cột như ngày, nhà cung cấp, địa điểm hoạt động kinh doanh, danh mục, thời gian ship, loại lỗi,...)

## Quy trình chuẩn bị dữ liệu
Dữ liệu được load và tải vào Tableau Public từ các file local sau khi đã thực hiện làm sạch hơn và fill các features cần thiết với python

**Chuẩn hoá:** Dữ liệu được load vào bảng, set up các relationship 
- **Bảng Order:** Ghi nhận các đơn giao dịch, ngày giờ và trạng thái đơn hàng
- **Bảng Order Items:** Thông tin chi tiết hơn về giá trị đơn hàng, các loại chi phí
- **Bảng Order Customers:** Các dạng thông tin chi tiết hơn về khách hàng
- **Một số bảng dim khác:** Thông tin sản phẩm, hình thức thanh toán, sellers và địa lý

<img width="1710" alt="image" src="https://github.com/user-attachments/assets/74c2753c-2c95-48cd-830b-9be7c13fd841" />

