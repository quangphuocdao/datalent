# Datalent
Đây là bản phân tích dữ liệu của nhóm Datalent được thực hiện bằng ngôn ngữ lập trình Python, tập trung vào bộ dữ liệu của doanh nghiệp phim. Mục đích của việc phân tích nhằm trích xuất, thống kê, và phân tích dữ liệu để đưa ra thông tin có giá trị. Những kết quả này đóng góp quan trọng vào quá trình đưa ra quyết định chiến lược cho doanh nghiệp, hỗ trợ việc tối ưu hóa các quy trình và tạo ra cơ sở cho quyết định thông tin đúng đắn dựa trên dữ liệu. 
# Quy trình xử lý bộ dữ liệu
1. Đọc file dữ liệu từ Excel (Raw data ở đây: [final_dataset.xlsx](https://github.com/quangphuocdao/datalent/files/14158925/final_dataset.xlsx))
   - File dữ liệu bao gồm: 4 trang sheets, 1 trang chính gồm tất cả những thông tin cần thiết để phục vụ cho mục đích phân tích, 3 trang còn lại để tham khảo thông tin.
   - Trang chính có tổng cột 27 cột (gồm: Mã order, Thu ngân, Ngày bán, Tổng, Ngày/Tháng/Năm sinh, Tuổi, Giới Tính, Quận/Huyện, Tỉnh, Công việc, Lĩnh vực, Mã khách hàng, Mã vé, Ngày, Thời gian, Chỗ ngồi, Phòng	Phim, Mã phim, Quốc gia, Thể loại phim, Phân loại phim, Thời lượng phim, Thể loại chỗ, Thể loại vé, Giá vé, Bỏng ngô)

2. Sau khi đọc file dữ liệu từ Excel:
   - Thực hiện các bước Data Cleaning [bao gồm: kiểm tra các giá trị trùng lặp (.distinct()), sửa các định dạng dữ liệu cho phù hợp (dùng pd.datetime), kiểm tra các giá trị khuyết thiếu (isna())...].
   - Tạo 1 bản sao để thực hiện việc làm sạch dữ liệu, để đảm bảo chắc chắn bản dữ liệu chính thức đã được làm sạch. Các thông tin sau khi được làm sạch sẽ đủ khả năng phục vụ cho việc phân tích.

5. 

