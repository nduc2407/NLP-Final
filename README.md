# NLP-Final

Đồ án dịch máy Anh - Pháp sử dụng mô hình **Seq2Seq với LSTM**. Project
so sánh hai cấu hình:

- Baseline Seq2Seq không có Attention.
- Seq2Seq có Attention và Beam Search khi suy luận.

## Dataset

Dữ liệu được chia thành ba tập `train`, `val` và `test`. Mỗi câu tiếng Anh
trong file `.en` tương ứng với câu tiếng Pháp cùng dòng trong file `.fr`.

## Cấu trúc project

```text
data/
├── train.en, train.fr
├── val.en, val.fr
└── test.en, test.fr

src/
├── main_baseline.ipynb    # Mô hình Seq2Seq không có Attention
├── main_attention.ipynb   # Mô hình Attention và Beam Search
├── best_model.pth         # Trọng số mô hình đã huấn luyện
├── loss_chart.png         # Biểu đồ loss
├── train_losses.npy       # Loss trên tập train
└── val_losses.npy         # Loss trên tập validation

report/
└── 3123410082_DangNhatDuc_DoAnCuoiKiNLP.pdf
```

## Cài đặt

Cài đặt Python 3.10 trở lên, sau đó cài các thư viện được sử dụng trong
notebook:

```bash
pip install torch numpy matplotlib nltk jupyter
```

## Cách chạy

1. Mở project bằng VS Code hoặc Jupyter Notebook.
2. Chọn kernel Python đã cài PyTorch.
3. Mở `src/main_baseline.ipynb` hoặc `src/main_attention.ipynb`.
4. Chạy các cell theo thứ tự từ trên xuống dưới.

Notebook sẽ đọc dữ liệu trong thư mục `data/`, huấn luyện mô hình và lưu
loss cùng trọng số mô hình vào thư mục `src/`.

## Kết quả

Các loss trong quá trình huấn luyện được lưu ở `src/train_losses.npy` và
`src/val_losses.npy`. Biểu đồ trực quan được lưu tại `src/loss_chart.png`.

## Báo cáo

Báo cáo đầy đủ của đồ án nằm tại
`report/3123410082_DangNhatDuc_DoAnCuoiKiNLP.pdf`.
