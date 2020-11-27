# FACE RECOGNITION REPORT

## Python Language:

### 1. YOLO v5:
>**Mô tả:**  Yolo là một mô hình mạng CNN cho việc phát hiện, nhận dạng, phân loại đối tượng. Yolo được tạo ra từ việc kết hợp giữa các convolutional layers và connected layers.Trong đóp các convolutional layers sẽ trích xuất ra các feature của ảnh, còn full-connected layers sẽ dự đoán ra xác suất đó và tọa độ của đối tượng.
* Link github: https://github.com/ultralytics/yolov5
>**Tính năng đã khai thác được:** Đã sử dụng để detect được mọi vật trong images, videos và webcam nhưng vẫn có sai số trong quá trình detect.
* Kết quả :

![Kết quả webcam](https://github.com/anhocva214/learn-computer-vision/blob/master/images/yolov5-webcam.jpg)

***Kết quả từ webcam***


![Kết quả từ ảnh](https://github.com/anhocva214/learn-computer-vision/blob/master/images/yolov5-image.png)

***Kết quả từ ảnh***

***Kết quả từ video:*** https://drive.google.com/file/d/1PX3KkM0XU0xqyUgQij_FSBfPrNgayCO1/view?usp=sharing

### 2. Face Recognition YOLO v3
>**Mô tả:** Sử dụng mô hình YOLO v3 để detect face trong ảnh, video và webcam

* Link github: https://github.com/sthanhng/yoloface

>**Tính năng đã khai thác được:** Đã sử dụng để detect được khuôn mặt trong images, videos và webcam nhưng tốc độ xử lý chậm

* Kết quả :

<!-- ***Kết quả từ video:*** https://drive.google.com/file/d/1PX3KkM0XU0xqyUgQij_FSBfPrNgayCO1/view?usp=sharing -->

![Kết quả từ ảnh](https://github.com/anhocva214/learn-computer-vision/blob/master/images/yolov3-image.jpg)

***Kết quả từ ảnh***

### 3. Face Recognition Using OpenCV
>**Mô tả:** source code sử dụng thư viện openCv và file haarcascade_frontalface_default.xml để detect và recognition face thông qua dataset khuôn mặt từng đối tượng từ webcam

* Link github: https://github.com/chandrikadeb7/Face-Recognition-in-Python

>**Tính năng đã khai thác được:** Đã sử dụng để detect và recognition được khuôn mặt trong webcam với tốc dộ nhanh nhưng độ chính xác không cao vào khoảng 30%-65%

* Kết quả:

![Dataset](https://github.com/anhocva214/learn-computer-vision/blob/master/images/opencv-dataset.jpg)

***Ảnh dataset***

![Ảnh dự đoán từ webcam](https://github.com/anhocva214/learn-computer-vision/blob/master/images/opencv-test.jpg)

***Ảnh dự đoán từ webcam***

## Javascript Language:

### 1. Face-api.js
>**Mô tả:** Sử dụng tensorflow và 1 số model đuợc build sẵn phục vụ cho: `Face Recognition`, `Face Landmark Detection`, `Face Expression Recognition`, `Age Estimation` và `Gender Recognition`.

* Link github: https://github.com/justadudewhohacks/face-api.js#face-api.js-for-the-browser

>**Tính năng đã khai thác được:** Tích hợp được cho web về chức năng `Face Recognition` và `Face Landmark Detection`, bên cạnh còn 1 số tính năng chưa tìm hiểu. 

>Mặc khác độ chính xác rừ 70-95% nhưng tốc độ hơi chậm vì camera chụp hình -> xử lý hình liên tục -> đưa ra kết qua liên tục. Mỗi lượt như vậy mất khoảng 700-1000ms.

* Kết quả:

![Face Recognition](https://github.com/anhocva214/learn-computer-vision/blob/master/images/faceapi-recognition.jpg)

***Face Recognition***

![Face Landmark](https://github.com/anhocva214/learn-computer-vision/blob/master/images/faceapi-landmark.jpg)

***Face Landmark***

