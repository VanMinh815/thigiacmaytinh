Lab 8: Video Object Detection
Tổng quan

Nhận diện đối tượng trong video bằng RetinaNet (ImageAI), xử lý theo thời gian thực và xuất video có bounding box + nhãn.

Nội dung chính
Cài đặt: imageai, torch, opencv, matplotlib
Tải model: RetinaNet pretrained (COCO)
Kiểm tra video: FPS, kích thước, số frame
Detect: dùng detectObjectsFromVideo()
Xuất video: video_detected.mp4
Hiển thị kết quả: lấy sample frames
Pipeline
Input Video → Load Model → Detect Objects → Output Video
Công nghệ
Python
ImageAI + RetinaNet
PyTorch
OpenCV
Matplotlib
Kết quả

Video đầu ra có:

Bounding box
Nhãn đối tượng
Confidence score