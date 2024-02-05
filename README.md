# Datalent
Đây là bản phân tích dữ liệu của nhóm Datalent, tập trung vào bộ dữ liệu của doanh nghiệp phim. Mục đích của việc phân tích nhằm trích xuất, thống kê, và phân tích dữ liệu để đưa ra thông tin có giá trị. Những kết quả này đóng góp quan trọng vào quá trình đưa ra quyết định chiến lược cho doanh nghiệp, hỗ trợ việc tối ưu hóa các quy trình và tạo ra cơ sở cho quyết định thông tin đúng đắn dựa trên dữ liệu. Các tài nguyên được sử dụng bao gồm Python và các gói liên quan Jupyter, matplotlib, Pandas, Numpy, Plotly và Seaborn. Tất cả các thư viện này đều được import qua Jupyter Notebook

# Quy trình xử lý bộ dữ liệu
1. Đọc file dữ liệu từ Excel (Raw data ở đây: [final_dataset.xlsx](https://github.com/quangphuocdao/datalent/files/14158925/final_dataset.xlsx))
   - File dữ liệu bao gồm: 4 trang sheets, 1 trang chính gồm tất cả những thông tin cần thiết để phục vụ cho mục đích phân tích, 3 trang còn lại để tham khảo thông tin.
   - Trang chính có tổng cột 27 cột (gồm: Mã order, Thu ngân, Ngày bán, Tổng, Ngày/Tháng/Năm sinh, Tuổi, Giới Tính, Quận/Huyện, Tỉnh, Công việc, Lĩnh vực, Mã khách hàng, Mã vé, Ngày, Thời gian, Chỗ ngồi, Phòng	Phim, Mã phim, Quốc gia, Thể loại phim, Phân loại phim, Thời lượng phim, Thể loại chỗ, Thể loại vé, Giá vé, Bỏng ngô)
   - Thực hiện quan sát 1 số giá trị ban đầu của bộ dữ liệu, và thống kê mô tả các giá trị numeric:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/72b43a69-c80e-45e3-b593-34e716432dad)
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/be3f76d0-5be8-4596-97a0-46d83087bf55)

   
2. Sau khi đọc file dữ liệu từ Excel:
   - Thực hiện các bước Data Cleaning [bao gồm: kiểm tra các giá trị trùng lặp (.distinct()), sửa các định dạng dữ liệu cho phù hợp (dùng pd.datetime), kiểm tra các giá trị khuyết thiếu (isna())...].
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/35be1b96-df98-4733-9db7-9321f43a369a)
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/73d2c27f-d061-4947-8198-c4899873266b)
   - Tạo 1 bản sao để thực hiện việc làm sạch dữ liệu, để đảm bảo chắc chắn bản dữ liệu chính thức đã được làm sạch. Các thông tin sau khi được làm sạch sẽ đủ khả năng phục vụ cho việc phân tích.
     

3. Thực hiện phân tích thống kê 1 số yêu cầu:
   - Phân tích thống kê tổng doanh thu và số lượng vé theo các ngày trong tháng 5/2019:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/977208fc-d867-454a-b84f-021308096d12)
   - Phân tích thống kê tổng doanh thu và số lượng vé được mua dựa theo thời gian bộ phim được chiếu:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/3d4072c7-04c8-4b97-8e37-697e39f27239)
   - Phân tích thống kê tổng doanh thu và số lượng vé được mua dựa theo nhóm tuổi của khách hàng:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/03db54f9-bde2-4983-a3f9-dde40000af78)
   - Phân tích thống kê tổng doanh thu và số lượng vé được bán ra dựa theo giới tính
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/ee618323-f641-4cb5-a285-42bd5583d384)
   - Phân tích thống kê tổng doanh thu dựa theo tỉnh thành:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/ba3c727e-6fa5-4d82-92b9-412e5d1375ed)
   - Phân tích thống kê tổng doanh thu và số lượng vé được mua dựa theo nghề nghiệp của khách hàng:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/bc214437-d31d-4531-96c8-3df7e53a019b)
   - Phân tích thống kê tổng doanh thu theo từng bộ phim:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/dd9327a3-8025-4e26-9074-85906eb023b1)
   - Phân tích thống kê doanh thu và số lượng vé được bán ra của từng thể loại phim:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/ce83f186-49bc-4c70-ade6-1931d7fb8ef7)
   - Phân tích thống kê tổng doanh thu và số lượng vé được bán ra dựa theo thời lượng của phim:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/fd35f918-acb0-410e-86c1-be670847ab26)
   - Phân tích thống kê số lượng popcorn được mua bởi khách hàng:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/42382643-810f-419d-b3af-be99a6204b33)
   - Phân tích thống kê doanh thu và số lượng vé được bán ra đối với phim của từng quốc gia:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/0f32b688-33a9-41f8-ac5f-3f1a1672f32b)
   - Phân tích thống kê số lượng khách hàng đi xem phim thì đi xem với mấy người:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/b7b08dbe-5e50-4217-b9ab-88a4283e3643)
   - Phân tích thống kê tổng doanh thu dựa theo giới tính và thể loại phim:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/b8b6ccd6-3bb3-4245-ba6f-039901a1011d)
   - Phân tích thống kê tổng doanh thu dựa vào giới tính và thể loại phim:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/b3052463-db0a-4650-91e8-88b76bd12b23)
   - Kiểm tra độ tương quan giữa các numeric values:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/f3467efe-62a0-4ddc-839e-21b8b4d56618)

# Kết luận:
Sau khi thực hiện các bước phân tích thống kê, team đã rút ra được nhiều insights có giá trị, từ đó nghiên cứu thêm các hướng giải quyết cho doanh nghiệp dựa theo những insights trên. Toàn bộ phần Data-Driven Decision Making, nhằm để tối ưu hóa tất cả các thông tin hữu ích từ việc nghiên cứu thị trường kết hợp phân tích dữ liệu, team Datalent sẽ thực hiện ở phần báo cáo.












