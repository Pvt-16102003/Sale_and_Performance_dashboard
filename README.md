# Sale Dashboard
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
<img width="1704" alt="Ảnh màn hình 2025-03-12 lúc 00 52 20" src="https://github.com/user-attachments/assets/71b32003-7593-462e-a0ee-86e462c14afd" />

## Phân tích dữ liệu 
### Tổng quan
<img width="1380" alt="Ảnh màn hình 2025-03-12 lúc 01 01 41" src="https://github.com/user-attachments/assets/f3ce1b10-1188-4bb4-a775-900c84671c71" />

Dashboard này cung cấp cái nhìn tổng thể về doanh số bán hàng trên nền tảng Olist trong năm 2018, giúp theo dõi hiệu suất kinh doanh, xu hướng doanh số, đơn hàng và số lượng khách hàng, cũng như đóng góp của các danh mục sản phẩm và các khu vực địa lý.

### Số liệu chính
- **Tổng doanh thu:** R$ 8,64M (Tăng 21,01% so với năm trước)
- **Giá trị đơn hàng trung bình (AOV):** R$ 160,04 (Tăng 1,05% so với năm trước)
- **Tổng số đơn hàng:** 54.011 (Tăng 19,76% so với năm trước)
- **Tổng số khách hàng:** 53.775 (Tăng 20,63% so với năm trước)

### Xu hướng doanh số theo tháng
- Biểu đồ thanh thể hiện tổng số doanh số theo tháng của năm hiện tại so với năm trước.
- Doanh số đạt đỉnh vào các tháng **Tháng 3 (1,16M), Tháng 4 (1,16M) và Tháng 5 (1,15M)**.
- Xu hướng suy giảm từ **Tháng 8 trở đi**, đặc biệt giảm mạnh vào **Tháng 9 và Tháng 10**.
- Điều này có thể cho thấy tác động của yếu tố mùa vụ hoặc các sự kiện ảnh hưởng đến nhu cầu khách hàng.

### Đóng góp doanh thu theo danh mục sản phẩm
(Tám danh mục sản phẩm hàng đầu chiếm **63,28%** tổng doanh số)
- **health_beauty**: R$ 0,89M (10,2%)
- **watches_gifts**: R$ 0,77M (8,9%)
- **bed_bath_table**: R$ 0,65M (7,5%)
- **sports_leisure**: R$ 0,62M (7,2%)
- **computers_accessories**: R$ 0,59M (6,9%)
- **housewares**: R$ 0,49M (5,7%)
- **furniture_decor**: R$ 0,48M (5,5%)
- **auto**: R$ 0,40M (4,7%)

### Hiệu suất bán hàng theo khu vực địa lý
(Năm bang hàng đầu chiếm **73,82%** tổng doanh số)
- **São Paulo (SP)**: R$ 5,92M (39,22%) - Tăng 34,89%
- **Rio de Janeiro (RJ)**: R$ 2,13M (12,37%) - Tăng 2,26%
- **Minas Gerais (MG)**: R$ 1,86M (11,65%) - Tăng 19,61%
- **Rio Grande do Sul (RS)**: R$ 0,89M (5,34%) - Tăng 9,25%
- **Paraná (PR)**: R$ 0,80M (5,24%) - Tăng 31,20%

### Phân tích tác động
- **Bang São Paulo đóng góp gần 40% tổng doanh thu**, cho thấy đây là khu vực thị trường quan trọng nhất.
- **Các bang phía Nam như RS và PR cũng có mức tăng trưởng mạnh, vượt 30%**.
- **Các danh mục sản phẩm liên quan đến sức khỏe, làm đẹp và quà tặng chiếm tỷ trọng cao**, cho thấy xu hướng mua sắm mạnh mẽ trong các ngành này.

### Nhận định
- **Sự tăng trưởng doanh số ổn định** nhưng có sự sụt giảm vào cuối năm, có thể cần các chương trình kích cầu để duy trì mức tăng trưởng.
- **Danh mục sản phẩm có đóng góp lớn nên được tập trung phát triển**, đặc biệt là **health_beauty, watches_gifts và sports_leisure**.
- **Các khu vực tiềm năng như RS và PR cần được khai thác mạnh hơn** để tận dụng đà tăng trưởng.


