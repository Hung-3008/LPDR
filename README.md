# LPDR - LICENSE PLATE DETECTION & RECOGNOTION
## 1. Thông tin nhóm 
| Name | ID |
| --------------- | --------------- | 
| Bui Van Hung | 19127414 | 
| Nguyen Thai Binh | 19127103 | 

## 2. Nội dung đồ án
Phát hiện và Nhận diện một số loại biển số xe ở Việt Nam

## 3. Quy trình chung
![alt text](https://github.com/Abramo-Cassano/LPDR/blob/main/images/flow-diagram.png?raw=true)

Đầu tiêm, chuẩn bị bộ dữ liệu được gán nhãn sẵn, sau đó sử dụng model "mobilenet_v2_fpnlite" của TensorFlow để huấn luyện. Kết quả sau bước này là vùng ảnh chứa biển số xe và tọa độ các đỉnh của biển số. Sau đó áp dụng Easy OCR để đọc các chữ có trên biển số đã detect được. 

## 4. Mô tả tập dữ liệu 
Trong đồ án này sử dụng bộ dữ liệu [Vietnamese License Plate Detection](https://github.com/winter2897/Real-time-Auto-License-Plate-Recognition-with-Jetson-Nano/blob/main/doc/dataset.md) của tác giả [Tran Hai Quan](https://github.com/winter2897)
Bộ dữ liệu gồm hơn 6000 bức ảnh chụp biển số xe ô tô và xe gắn máy với nhiều góc độ và điều kiện thời tiết khác nhau. Dữ liệu được gán nhãn theo định dạng VOC/PASCAL hoặc YOLO. 

![alt text](https://github.com/Abramo-Cassano/LPDR/blob/main/images/plate_dataset.png?raw=true)

Link download: 
| Dataset | VOC/PASCAL | YOLO |
| --------------- | --------------- | ---------------|
| Vietnamese License Plate Detection   | [Link](https://drive.google.com/file/d/1irJC4V4IlxJJKOtJX1u0LZSSUrKjjgTq/view?usp=sharing) | [Link](https://drive.google.com/file/d/1KLK-DWgT3VoQH4fcTxAt2eB3sm7DGWAf/view?usp=sharing)|

## 5. Kết quả thực nghiệm
### 5.1 Thực nghiệm trên ảnh đơn 

Phát hiện biển số xe từ ảnh input

![alt text](https://github.com/Abramo-Cassano/LPDR/blob/main/images/detectplate.png?raw=true)

Đọc ký tự trên biển số xe:

![alt text](https://github.com/Abramo-Cassano/LPDR/blob/main/images/OCR.png?raw=true)

### 5.1 Thực nghiệm trong thời gian thực

