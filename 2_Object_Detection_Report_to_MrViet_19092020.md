# OBJECT DETECTION REPORT

Object detection đóng vai trò quan trọng trong lĩnh vực computer vision, vì đa số các ứng dụng trong lĩnh vực này đều sử dụng những mô hình, kiến trúc object detection như CNN, R-CNN, Faster R-CNN,…).

Sau khi deep learning ra đời thì xuất hiện một số mô hình, kiến trúc object detection mang độ chính xác cao và nhanh hơn so với các mô hình cổ điển thậm chí là real-time như là YOLO, RetinaNet,…

Vấn đề trong kiến trúc RetinaNet là anchor-based. Và đây cũng là nhược điểm cụ thể là có một số ground truth object không được gán cho bất kì anchor vì độ phủ không vượt quá ngưỡng xác định. Đây cũng là vấn đề ảnh hưởng đến quá trình huấn luyện và thử nghiệm mang lại độ chính xác thấp.

Để giải quyết vấn đề này một framework mới đã được đề xuất là FCOS, nó không sử dụng anchor để xét ground truth object mà sử dụng một chiến lược mẫu, với sự thay thế đó framework FCOS không chỉ nhanh hơn mà con chính xác hơn RetinaNet

Với sư quan sát này, PIF Lab có một phát triển mới về mô hình object detection dựa trên FCOS. Mục tiêu của họ là một mô hình mới có độ chính xác giống như FCOS nguyên bản nhưng chạy nhanh hơn. Chiến lược của họ là thay thế backbone với lightweight-yet-powerful backbone khác, họ cũng áp dụng những loss function nâng cao để giải quyết một số vấn đề đặc biệt.
