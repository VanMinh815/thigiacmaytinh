1. Mục tiêu
Thực hiện lọc không gian (Spatial Filtering)
So sánh PIL và OpenCV
Phát hiện đặc trưng ảnh (Feature Detection)
2. Nội dung chính
2.1. Lọc không gian
a. Lọc tuyến tính
Mean Filter: làm mờ, giảm nhiễu
Gaussian Blur: mượt hơn, giữ cạnh tốt hơn
Sharpening: làm nét ảnh bằng kernel

Thư viện:

PIL: ImageFilter.BLUR, GaussianBlur, SHARPEN
OpenCV: cv2.filter2D(), cv2.GaussianBlur()
b. Phát hiện cạnh (Edge Detection)
Dựa trên sự thay đổi cường độ pixel
Sobel: phát hiện cạnh theo X, Y

Thư viện:

PIL: FIND_EDGES
OpenCV: cv2.Sobel()
c. Median Filter (Phi tuyến tính)
Lấy trung vị để khử nhiễu salt-pepper
Giữ cạnh tốt

Thư viện:

PIL: MedianFilter
OpenCV: cv2.medianBlur()
d. Threshold (OpenCV)
Chuyển ảnh thành trắng/đen theo ngưỡng
Dùng để tách đối tượng

Hàm: cv2.threshold()

2.2. Phát hiện đặc trưng (Feature Detection)
Harris Corner: phát hiện góc
SIFT: đặc trưng không đổi theo scale & rotation
Keypoints & Descriptors: dùng để so khớp ảnh

Ứng dụng:

Nhận dạng đối tượng
Ghép ảnh panorama
Tracking
2.3. So sánh PIL và OpenCV
Tiêu chí	PIL	OpenCV
Màu	RGB	BGR
Dữ liệu	Image	NumPy
Dễ dùng	Dễ	Khó hơn
Tùy biến	Ít	Nhiều
Hiệu năng	Thấp hơn	Cao hơn
Ứng dụng	Cơ bản	Nâng cao
3. Kết luận
Hiểu các bộ lọc: Mean, Gaussian, Median, Sharpen
Biết tích chập (convolution) và kernel
Phát hiện cạnh bằng Sobel
Áp dụng threshold để phân vùng ảnh
Nắm cơ bản Feature Detection
4. Công cụ
Python
PIL / OpenCV
NumPy
Matplotlib