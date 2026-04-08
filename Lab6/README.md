1. Mục tiêu
Phát hiện điểm đặc trưng (keypoint)
Hiểu SIFT (bất biến scale, rotation)
Ứng dụng vào matching, panorama, CBIR
2. Nội dung chính
2.1. Harris Corner
Phát hiện góc dựa trên thay đổi cường độ
Giá trị R:
R > 0: corner
R < 0: edge

Hàm: cv2.cornerHarris()

2.2. DoG (Difference of Gaussians)
Lấy hiệu 2 ảnh Gaussian khác sigma
Dùng để phát hiện đặc trưng ở nhiều scale

→ Sigma nhỏ: chi tiết
→ Sigma lớn: tổng thể

2.3. Scale Selection
Tìm scale tốt nhất cho mỗi pixel
Dựa trên cực đại của LoG

→ Giúp phát hiện đặc trưng đa kích thước

2.4. SIFT
Phát hiện keypoint bất biến scale & rotation
Descriptor: 128 chiều

Hàm: cv2.SIFT_create()

2.5. Blob Detection
Phát hiện vùng tròn (blob)
Dùng cv2.SimpleBlobDetector
2.6. Bag of Words (BoW)
Trích xuất SIFT descriptor
Gom nhóm (KMeans) → visual words
Biểu diễn ảnh bằng histogram

→ Dùng để so sánh ảnh

2.7. Panorama
Match keypoint giữa 2 ảnh
Dùng Homography + RANSAC để ghép
2.8. CBIR
So sánh ảnh bằng histogram BoW
Dùng Cosine Similarity

→ Tìm ảnh giống nhau

3. So sánh phương pháp
Phương pháp	Scale	Rotation	Ứng dụng
Harris	✗	Một phần	Góc
DoG	✓	✗	Scale
SIFT	✓	✓	Matching
Blob	✓	✓	Shape
4. Kết luận
Hiểu Harris, DoG, SIFT
Biết chọn scale phù hợp
Áp dụng keypoint vào matching, panorama
Xây dựng BoW và CBIR cơ bản
5. Công cụ
Python
OpenCV
NumPy
Matplotlib