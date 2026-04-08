1. Mục tiêu
Thực hiện các phép biến đổi hình học trên ảnh
Áp dụng phép toán mảng và ma trận
So sánh PIL (Pillow) và OpenCV
Nén ảnh bằng SVD
2. Nội dung chính
2.1. Biến đổi hình học
Scaling (Resize):
Phóng to/thu nhỏ ảnh bằng nội suy (nearest, bilinear, bicubic)
Translation (Dịch chuyển):
Di chuyển ảnh theo trục x, y bằng ma trận affine
Rotation (Xoay):
Xoay ảnh theo góc bất kỳ, có thể giữ nguyên khung ảnh

Thư viện sử dụng:

PIL: resize(), rotate(), transform()
OpenCV: cv2.resize(), cv2.warpAffine()
2.2. Phép toán trên ảnh
a. Phép toán mảng
Cộng, trừ, nhân, chia pixel
Điều chỉnh độ sáng và độ tương phản
Trộn ảnh (blending)
Phép logic: AND, OR, XOR, NOT
b. Phép toán ma trận (SVD)
Phân rã: A = U × Σ × Vᵀ
Giữ k giá trị lớn nhất để nén ảnh

Kết quả:

k nhỏ → ảnh mờ
k lớn → ảnh rõ, gần giống ảnh gốc

Ý nghĩa: giảm dung lượng, giữ đặc trưng quan trọng

2.3. So sánh PIL và OpenCV
Tiêu chí	PIL	OpenCV
Màu	RGB	BGR
Dữ liệu	Image	NumPy
Dễ dùng	Dễ	Khó hơn
Hiệu năng	Thấp hơn	Cao hơn
Ứng dụng	Cơ bản	Nâng cao
2.4. Lab 02 – Filters
Averaging, Gaussian: làm mờ
Median: khử nhiễu
Bilateral: mờ nhưng giữ cạnh
Sharpening: làm nét
Filter2D: kernel tùy chỉnh

Khác:

Crop ảnh
Bitwise operations
Image blending
3. Kết luận
Hiểu các phép biến đổi: resize, dịch, xoay
Biết dùng ma trận affine
Áp dụng phép toán trên ảnh
Hiểu SVD để nén ảnh
Phân biệt PIL và OpenCV
4. Công cụ
Python
PIL / OpenCV
NumPy
Matplotlib