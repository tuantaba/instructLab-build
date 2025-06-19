# instructLab-build
instruct - means instruction 
Lab - laboratory

"Phòng thí nghiệm về huấn luyện mô hình theo hướng chỉ dẫn", hay nói cách khác, là nền tảng mở để tùy biến LLMs thông qua việc hướng dẫn (instruction-tuning) và bổ sung kiến thức mới.
"instructLab" = nơi bạn có thể hướng dẫn mô hình học hỏi những gì bạn muốn, theo cách mở, có kiểm soát, và dễ tùy biến.


# Granite
Granite LLM là một dòng mô hình ngôn ngữ lớn (Large Language Models – LLMs) mã nguồn mở do IBM phát triển, được thiết kế đặc biệt cho các ứng dụng doanh nghiệp và tích hợp sâu với hệ sinh thái Red Hat AI như RHEL AI và OpenShift AI.

## Granite có gì đặc biệt
Mã nguồn mở & minh bạch: Granite được phát hành theo giấy phép Apache 2.0, cho phép bạn tùy chỉnh, triển khai và kiểm soát hoàn toàn mô hình. IBM còn công bố phần lớn dữ liệu huấn luyện, giúp tăng độ tin cậy.

Hỗ trợ đa nhiệm vụ: Granite có thể xử lý cả ngôn ngữ tự nhiên và mã lập trình, phù hợp cho các tác vụ như chatbot, phân tích văn bản, sinh mã, tóm tắt, và nhiều hơn nữa.

Tối ưu cho doanh nghiệp: Granite được huấn luyện với dữ liệu đã chọn lọc kỹ, đảm bảo an toàn và hiệu suất cao trong môi trường doanh nghiệp. Không giống các mô hình AI công cộng, Granite không tiếp tục huấn luyện sau khi triển khai, nên dữ liệu của bạn không bị chia sẻ ngược lại

## Các phiên bản Granite
Granite có nhiều kích thước mô hình, từ nhỏ gọn (sub-billion parameters) đến lớn (34B), phù hợp với nhiều nhu cầu và hạ tầng khác nhau. Một số phiên bản còn được tinh chỉnh sẵn (instruction-tuned) để hiểu và làm theo hướng dẫn tốt hơn.


## How to setup & use instructLab
Bước 1: Cài đặt InstructLab
pip install instructlab
from GIT Repo: github.com/instructlab/instructlab

Bước 2: Tải mô hình nền Granite
ilab model get
Chọn một mô hình Granite phù hợp, ví dụ granite-3b-code hoặc granite-3b-chat.


Bước 3: Tạo “kỹ năng” (skill) riêng
Bạn có thể định nghĩa một kỹ năng bằng cách thêm các cặp câu hỏi - câu trả lời:
ilab skill add --name "chat-tu-van" --input "Làm sao để tiết kiệm điện?" --output "Bạn có thể sử dụng bóng đèn LED, tắt thiết bị khi không dùng..."

Bước 4: Sinh dữ liệu & huấn luyện mô hình
ilab data build
ilab train

Bước 5: Chạy thử mô hình
ilab chat

## Bonus
Dùng Taxonomy UI để quản lý cây kỹ năng trực quan.
Kết hợp với RHEL AI để huấn luyện mô hình hiệu quả trên GPU hoặc môi trường doanh nghiệp.




