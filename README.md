# 🐾 Mô hình Deep Learning bằng Keras để nhận diện Chó, Mèo và Ngựa

Dự án này xây dựng một mô hình học sâu sử dụng **Keras** và kiến trúc **CNN (Convolutional Neural Network)** để phân loại hình ảnh của ba loài vật: **chó**, **mèo** và **ngựa**.

---

## 📦 Tải Dataset

Vì dung lượng dataset khá lớn, bạn vui lòng tải thủ công từ Google Drive theo đường dẫn sau:

🔗 **[Tải Dataset từ Google Drive](https://drive.google.com/drive/folders/1v0GWNR_spJMUY24n9VLlm2kwhqRXepj9?usp=sharing)**

Sau khi tải về và giải nén, hãy đặt thư mục dữ liệu vào trong thư mục `data/` theo cấu trúc sau:

data/
├── train/
│ ├── dog/
│ ├── cat/
│ └── horse/
└── validation/
├── dog/
├── cat/
└── horse/

yaml
Sao chép
Chỉnh sửa

---

## 🚀 Tính năng nổi bật

- Sử dụng **TensorFlow** và **Keras**
- Huấn luyện mô hình CNN từ đầu hoặc từ mô hình pretrained
- Tăng cường dữ liệu (augmentation) để cải thiện độ chính xác
- Lưu mô hình tốt nhất và đánh giá bằng các chỉ số như accuracy và confusion matrix
- Có thể mở rộng thêm lớp mới chỉ với vài chỉnh sửa nhỏ

---

## ⚙️ Cài đặt và chạy mô hình

### 1. Cài đặt thư viện
bash
pip install -r requirements.txt
2. Huấn luyện mô hình
bash
Sao chép
Chỉnh sửa
python src/train.py \
  --data_dir data/ \
  --epochs 30 \
  --batch_size 32 \
  --img_size 224
3. Đánh giá mô hình
bash
Sao chép
Chỉnh sửa
python src/evaluate.py \
  --model_path model/best_model.h5 \
  --data_dir data/validation/
📊 Kết quả
Mô hình đạt độ chính xác cao (~90%) trên tập validation

Có thể đánh giá thêm bằng các biểu đồ loss/accuracy và ma trận nhầm lẫn

🧠 Yêu cầu hệ thống
Python 3.7+

TensorFlow 2.x

numpy, matplotlib, scikit-learn

📜 Giấy phép
Dự án được phát hành theo giấy phép MIT – bạn được phép tự do sử dụng, chỉnh sửa và phân phối.
