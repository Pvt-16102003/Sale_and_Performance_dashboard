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

# Olist Sale Dashboard 
<img width="1380" alt="Ảnh màn hình 2025-03-12 lúc 01 31 31" src="https://github.com/user-attachments/assets/7896bfa1-51d2-42a6-a4f7-43a36e5a0b57" />
## Mục đích của Dashboard

Dashboard này cung cấp cái nhìn tổng quan về hiệu suất bán hàng trên nền tảng Olist, giúp người dùng:

- **Theo dõi tổng doanh thu và tổng số đơn hàng**, so sánh với cùng kỳ năm trước để đánh giá xu hướng tăng trưởng.
- **Phân tích xu hướng bán hàng theo tháng**, nhận diện thời điểm có sự biến động đáng kể trong doanh số.
- **Đánh giá tác động của các danh mục sản phẩm khác nhau** đến tổng doanh thu và xác định ngành hàng tiềm năng.
- **Xác định khu vực địa lý có đóng góp lớn nhất** vào doanh số, từ đó hỗ trợ chiến lược mở rộng thị trường.
- **So sánh mối quan hệ giữa giá hiển thị và doanh số**, giúp tối ưu chiến lược định giá sản phẩm.

## Số liệu chính
- **Tổng doanh thu:** R$ 8,64M (tăng 21,01% so với năm trước)
- **Tổng số đơn hàng:** 54.011 đơn (tăng 19,76% so với năm trước)
- **Giá trị trung bình trên mỗi đơn hàng (AOV):** R$ 160,04 (tăng 1,05% so với năm trước)

## Phân tích xu hướng doanh số

### 1. Doanh số theo thời gian

- **Biểu đồ cột hiển thị tổng số đơn hàng và doanh thu theo từng tháng**, giúp xác định xu hướng theo mùa.
- **Doanh số có xu hướng đạt đỉnh vào tháng 3, 4, 7 và giảm mạnh vào các tháng cuối năm**, có thể do ảnh hưởng từ thói quen mua sắm hoặc yếu tố kinh tế vĩ mô.
- **Tổng đơn hàng có sự biến động đồng bộ với doanh số**, cho thấy mức tăng trưởng chủ yếu đến từ số lượng đơn hàng hơn là giá trị trung bình trên mỗi đơn hàng.

### 2. Phân tích theo danh mục sản phẩm

- **Top 10 danh mục sản phẩm có doanh số cao nhất** gồm:
  1. Health & Beauty (0,885M)
  2. Watches & Gifts (0,772M)
  3. Bed & Bath (0,651M)
  4. Sports & Leisure (0,622M)
  5. Computers & Accessories (0,595M)
  6. Housewares (0,492M)
  7. Furniture & Decor (0,476M)
  8. Auto (0,404M)
  9. Baby (0,299M)
  10. Cool Stuff (0,274M)

- **Danh mục Health & Beauty dẫn đầu về doanh số**, chiếm tỷ trọng lớn trong tổng doanh thu của nền tảng.
- **Watches & Gifts và Sports & Leisure cũng có mức tăng trưởng cao**, cho thấy nhu cầu mạnh mẽ với các sản phẩm quà tặng và thể thao.
- **Danh mục Furniture & Decor và Housewares có tiềm năng nhưng chưa tăng trưởng mạnh**, có thể xem xét các chương trình khuyến mãi để kích thích nhu cầu.

### 3. Mối quan hệ giữa giá bán và doanh số

- **Biểu đồ phân tán thể hiện mối quan hệ giữa giá hiển thị và số lượng sản phẩm bán ra**.
- **Các danh mục sản phẩm có giá thấp hơn thường có doanh số cao hơn**, nhưng có một số danh mục giá cao vẫn đạt doanh số tốt (ví dụ: Home Appliances và Computers).
- **Có thể điều chỉnh chiến lược giá để tối ưu hóa lợi nhuận mà không làm giảm số lượng đơn hàng**.

## Shipment Quality Dashboard
<img width="1381" alt="Ảnh màn hình 2025-03-12 lúc 01 45 45" src="https://github.com/user-attachments/assets/d2b80ed8-4dd1-4316-b057-5be072518a8c" />

### Mục đích của Dashboard

Dashboard này cung cấp cái nhìn tổng quan về chất lượng giao hàng, giúp người dùng:

- **Theo dõi tổng số đơn hàng và tỷ lệ giao hàng trễ**, đánh giá xu hướng thay đổi theo thời gian.
- **Phân tích thời gian xử lý đơn hàng trung bình**, từ lúc đặt hàng đến khi duyệt và giao hàng cho khách.
- **Xác định các danh mục sản phẩm có tỷ lệ giao hàng trễ cao nhất**, hỗ trợ cải thiện quy trình vận chuyển.
- **Đánh giá tác động của từng bang đến tổng số đơn hàng và tỷ lệ giao hàng chậm**, giúp tối ưu hóa chuỗi cung ứng.
- **Xem chi tiết từng đơn hàng**, bao gồm thời gian đặt hàng, trạng thái giao hàng, phí vận chuyển và giá trị đơn hàng.

### Số liệu chính

- **Tổng số đơn hàng:** 54.011 (tăng 19,76% so với năm trước)
- **Thời gian xử lý trung bình:** 25,18 giờ (tăng 1,27%)
- **Số ngày giao hàng trung bình:** 11,55 ngày (giảm 1,12%)
- **Tỷ lệ giao hàng trễ:** 10,08% (tăng 69,29%)

### Phân tích xu hướng

### 1. Xu hướng giao hàng theo tháng

- **Biểu đồ xu hướng hàng tháng hiển thị số lượng đơn hàng, thời gian xử lý và tỷ lệ giao hàng trễ**.
- **Các tháng đầu năm có tỷ lệ giao hàng trễ cao hơn so với các tháng cuối năm**, cho thấy sự thay đổi trong hiệu suất giao hàng theo mùa.
- **Tháng 2 và tháng 4 có tỷ lệ giao hàng trễ cao nhất**, có thể do ảnh hưởng từ sự gia tăng đột biến trong số lượng đơn hàng hoặc các vấn đề trong chuỗi cung ứng.

### 2. Phân tích theo bang

- **Biểu đồ bản đồ thể hiện số lượng đơn hàng và tỷ lệ giao hàng trễ theo từng bang**.
- **Các bang có số lượng đơn hàng cao nhất**: SP, MG, RJ, RS.
- **Những bang có tỷ lệ giao hàng trễ cao nhất**: PE, PA, CE, MA, RN.
- **Cần tập trung vào các bang có tỷ lệ giao hàng trễ cao để cải thiện quy trình vận chuyển**.

### 3. Phân tích theo danh mục sản phẩm

- **Top 10 danh mục có tỷ lệ giao hàng trễ cao nhất**:
  1. Home Comfort (43%)
  2. Fashion Underwear (21%)
  3. Tablets & Printers (20%)
  4. Furniture (20%)
  5. Fashion & Sports (20%)
  6. Christmas Supplies (18%)
  7. Audio (14%)
  8. Office Furniture (12%)
  9. Computers (12%)
  10. Garden Tools (12%)

- **Home Comfort có tỷ lệ giao hàng trễ cao nhất (43%)**, cần được xem xét lại quy trình cung ứng và giao hàng.
- **Các sản phẩm liên quan đến công nghệ và nội thất cũng có tỷ lệ giao hàng trễ cao**, có thể do thời gian sản xuất và vận chuyển kéo dài.

### 4. Chi tiết đơn hàng

- **Danh sách chi tiết các đơn hàng bao gồm mã đơn hàng, ngày đặt, trạng thái giao hàng, phí vận chuyển và giá trị đơn hàng**.
- **Cho phép phân tích cụ thể từng đơn hàng để xác định nguyên nhân giao hàng trễ**.

### Nhận định

- **Số lượng đơn hàng tăng trưởng nhưng tỷ lệ giao hàng trễ cũng gia tăng**, cần có giải pháp tối ưu hóa logistics.
- **Các bang như PE, PA, CE có tỷ lệ giao hàng trễ cao nhất**, cần tập trung cải thiện dịch vụ vận chuyển tại đây.
- **Danh mục Home Comfort có tỷ lệ giao hàng trễ cao nhất**, có thể do quy trình sản xuất hoặc vận chuyển gặp vấn đề.
- **Các tháng đầu năm có tỷ lệ giao hàng trễ cao hơn**, có thể cần điều chỉnh nguồn lực theo mùa.


## Kết luận
Hiện tại, vẫn còn một số thiếu hụt về thông tin chi tiết, chẳng hạn như nguyên nhân cụ thể của việc giao hàng trễ theo từng khu vực hoặc danh mục sản phẩm, hay các thông tin về lợi nhuận trong quá trình kinh doanh để tiến hành một số phân tích sâu hơn và toàn diện hơn. Trong tương lai, chúng tôi sẽ tiếp tục cải thiện và bổ sung thêm dữ liệu để mang đến cái nhìn toàn diện hơn.
