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
   - Thống kê tổng doanh thu và số lượng vé theo các ngày trong tháng 5/2019:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/977208fc-d867-454a-b84f-021308096d12)
   - Thống kê tổng doanh thu và số lượng vé được mua dựa theo thời gian bộ phim được chiếu:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/3d4072c7-04c8-4b97-8e37-697e39f27239)
   - Thống kê tổng doanh thu và số lượng vé được mua dựa theo nhóm tuổi của khách hàng:
     ![image](https://github.com/quangphuocdao/datalent/assets/142654527/03db54f9-bde2-4983-a3f9-dde40000af78)



