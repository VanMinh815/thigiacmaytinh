1. Mục tiêu
Phân đoạn ảnh (Segmentation)
Nhận diện đối tượng (Detection) bằng Haar Cascade
2. Nội dung chính
2.1. Image Segmentation
a. Thresholding
Phân ảnh theo ngưỡng
Các loại: Binary, Inverse, Adaptive (Mean, Gaussian)
b. Otsu
Tự động chọn ngưỡng tối ưu
Phù hợp ảnh có 2 vùng sáng/tối rõ
c. K-Means
Phân cụm pixel theo màu
K lớn → chi tiết hơn nhưng chậm
d. Region Growing
Mở rộng vùng từ seed point
Dựa vào độ tương đồng pixel
e. Split & Merge
Chia ảnh thành vùng nhỏ (quadtree)
Gộp lại nếu đồng nhất
f. Edge-based
Phân đoạn theo cạnh
Dùng: Sobel, Laplacian, Canny, Watershed
2.2. Image Detection (Haar Cascade)
a. Detect STOP sign
Dùng CascadeClassifier
Phát hiện và vẽ bounding box
b. Face Detection
Dùng haarcascade_frontalface_default.xml
Điều chỉnh: scaleFactor, minNeighbors
c. Detect Eyes & Smile
Xác định trong vùng khuôn mặt (ROI)
Dùng file XML tương ứng
d. Detect Nose & Mouth
Tìm trong vùng phù hợp của khuôn mặt
3. So sánh Segmentation
Phương pháp	Ưu	Nhược
Threshold	Nhanh	Nhạy ánh sáng
Otsu	Tự động	Chỉ tốt với 2 lớp
K-Means	Linh hoạt	Chậm
Region Growing	Chính xác	Phụ thuộc seed
Split-Merge	Không cần seed	Tốn tài nguyên
Edge-based	Rõ biên	Nhiễu
4. Kết luận
Hiểu các phương pháp phân đoạn ảnh
Biết dùng K-Means, Otsu, Canny
Nhận diện đối tượng bằng Haar Cascade
Áp dụng vào bài toán thực tế
5. Công cụ
Python
OpenCV
NumPy
Matplotlib
scikit-learn