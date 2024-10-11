# Chẩn đoán Ung thư vú Sử dụng Mô hình Cây Quyết định và KNN

## Thành viên nhóm

- Vũ Đức Anh - Mã số sinh viên: 1671020036 - anhvuduc9204@gmail.com  
- Nguyễn Quang Hiệp - Mã số sinh viên: 1671020115 - quanghiep2342004@gmail.com  
- Võ Vĩnh Thái - Mã số sinh viên: 1671020289 - vovinhthai2004@gmail.com  

## Mục lục

1. [Giới thiệu Bài toán](#giới-thiệu-bài-toán)
2. [Phương pháp](#phương-pháp)
3. [Kết quả](#kết-quả)
4. [Công nghệ sử dụng](#công-nghệ-sử-dụng)
5. [Hướng dẫn sử dụng](#hướng-dẫn-sử-dụng)
6. [Hướng dẫn tải lên GitHub](#hướng-dẫn-tải-lên-github)
7. [Giấy phép](#giấy-phép)
8. [Đóng góp](#đóng-góp)

## Giới thiệu Bài toán

Ung thư vú là một trong những loại ung thư phổ biến nhất ở phụ nữ trên toàn thế giới. Chẩn đoán sớm đóng vai trò quan trọng trong việc nâng cao hiệu quả điều trị. Trong dự án này, chúng tôi đặt mục tiêu xây dựng hai mô hình đơn giản giúp các bác sĩ xác định khối u là lành tính (không ung thư) hay ác tính (ung thư) dựa trên dữ liệu của bệnh nhân: mô hình cây quyết định và mô hình KNN (K-Nearest Neighbors). Bằng cách áp dụng những mô hình này, chúng tôi hy vọng sẽ hỗ trợ các chuyên gia y tế trong việc đưa ra quyết định tốt hơn cho bệnh nhân của họ.

## Phương pháp

### 1. Cây Quyết định

Để giải quyết bài toán, chúng tôi sử dụng mô hình **cây quyết định** với các bước thực hiện như sau:

- **Thu thập và tiền xử lý dữ liệu**: 
  - Dữ liệu được sử dụng là **Bộ dữ liệu ung thư vú Wisconsin**.
  - Tiền xử lý bao gồm xử lý giá trị thiếu và chia tập dữ liệu thành hai phần: tập huấn luyện (80%) và tập kiểm tra (20%).
  
- **Xây dựng mô hình**: 
  - Sử dụng thuật toán ID3 hoặc C4.5, dựa trên các chỉ số Entropy hoặc Gini để chọn đặc trưng phân tách tốt nhất.
  
- **Huấn luyện mô hình**: 
  - Mô hình cây quyết định được huấn luyện trên tập dữ liệu huấn luyện để học cách phân loại chính xác khối u.
  
- **Đánh giá và tối ưu hóa mô hình**: 
  - Đánh giá mô hình trên các chỉ số: độ chính xác (accuracy), độ nhạy (recall), độ đặc hiệu (specificity), và điểm F1 (F1-score). 
  - Thực hiện cắt tỉa cây (pruning) để giảm hiện tượng quá khớp.

### 2. KNN (K-Nearest Neighbors)

Chúng tôi cũng triển khai mô hình **KNN** để phân loại khối u:

- **Thu thập và tiền xử lý dữ liệu**: 
  - Sử dụng cùng một bộ dữ liệu như trên và thực hiện tiền xử lý tương tự.
  
- **Huấn luyện mô hình**: 
  - Mô hình KNN được huấn luyện trên tập dữ liệu huấn luyện để phân loại khối u dựa trên k hàng xóm gần nhất.
  
- **Đánh giá mô hình**: 
  - Đánh giá mô hình KNN trên các chỉ số tương tự như mô hình cây quyết định.

## Kết quả

Cả hai mô hình (Cây Quyết định và KNN) đã chứng minh khả năng hỗ trợ hiệu quả trong chẩn đoán ung thư vú. Các chỉ số đánh giá mô hình cho thấy độ chính xác cao trong việc phân loại khối u. Kết quả cụ thể sẽ được in ra trong terminal khi chạy mô hình.

## Công nghệ sử dụng

- **Ngôn ngữ lập trình**: Python
- **Thư viện**: Scikit-learn, Pandas, NumPy, Seaborn, Matplotlib
- **Nguồn dữ liệu**: Bộ dữ liệu ung thư vú Wisconsin

## Hướng dẫn sử dụng

1. **Clone kho lưu trữ về máy tính của bạn** bằng cách sử dụng:

   ```bash
   git clone <repository-url>

2. Cài đặt các gói yêu cầu bằng cách chạy:
   
    pip install -r requirements.txt

3. Chạy mã để huấn luyện mô hình:
   
- Mở terminal và điều hướng đến thư mục dự án.
- Chạy script Python:

   python main.py

4. Kiểm tra kết quả được in ra trong terminal để xem hiệu suất của mô hình.

Hướng dẫn tải lên GitHub
Tạo tệp README.md:

Mở một trình soạn thảo văn bản (như Notepad, Visual Studio Code, hoặc bất kỳ trình soạn thảo nào bạn thích).
Sao chép và dán nội dung trên vào tệp và lưu lại với tên README.md.
Tải lên GitHub:

Vào kho lưu trữ GitHub của bạn.
Nhấn vào nút "Add file" (Thêm tệp) và chọn "Upload files" (Tải lên tệp).
Kéo và thả tệp README.md vào khu vực tải lên hoặc chọn tệp từ máy tính của bạn.
Nhấn "Commit changes" (Cam kết thay đổi) để lưu tệp vào kho lưu trữ.
Giấy phép
Dự án này sử dụng giấy phép MIT. Bạn có thể tự do sử dụng và chỉnh sửa mã nguồn, miễn là bạn giữ thông báo bản quyền trong mã.

Đóng góp
Nếu bạn muốn đóng góp cho dự án này, hãy làm theo các bước sau:

Fork kho lưu trữ về tài khoản của bạn.
Thực hiện các thay đổi và kiểm tra kỹ lưỡng.
Gửi yêu cầu kéo (pull request) với mô tả về các thay đổi của bạn.
Chúng tôi chào đón mọi đóng góp và đánh giá cao sự quan tâm của bạn đến việc cải thiện dự án này!


### Ghi chú
- Bạn có thể thay thế `<repository-url>` bằng URL thực tế của kho lưu trữ của bạn.
- Nếu có thêm thông tin chi tiết nào về kết quả hoặc bất kỳ phần nào khác bạn muốn cập nhật, hãy cho tôi biết để thêm vào.
