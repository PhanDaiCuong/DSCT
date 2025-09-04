# DSCT — Stock Forecasting (Dự án phân tích chứng khoán)

> Repo này chứa **mã nguồn** cho các pipeline tiền xử lý, huấn luyện và đánh giá mô hình time-series (Transformer) dùng cho dữ liệu chứng khoán.
---

## Mục tiêu dự án

Mục tiêu của nhóm là: **xây dựng pipeline dự báo cổ phiếu** dựa trên dữ liệu lịch sử và kỹ thuật (technical indicators) để xác định những cổ phiếu "đạt chuẩn và tốt" (có khả năng giữ/đạt các tiêu chí đầu tư do nhóm định nghĩa).

Nhiệm vụ chính:

* Tiền xử lý dữ liệu chứng khoán (merge, feature engineering, technical indicators).
* Huấn luyện mô hình Transformer cho chuỗi thời gian (xem thư mục `Time-Series-Transformer-Pytorch`).
* Sinh ra các tiêu chí/ranking để lựa chọn cổ phiếu "đạt chuẩn".

---

## Cấu trúc đề xuất của repository

```
DSCT/
├── Time-Series-Transformer-Pytorch/    # code chạy chính cho transformer (submodule hoặc thư mục)
├── Crawl-And-Fill                      # Crawl data from FiinQuant library 
├── report.html                         # Report about data trainning
├── requirements.txt                    # Required library
└── README.md
```

---

## Link download:

* **Dataset** (Google Drive):

  [Tải data tại đây](https://drive.google.com/drive/folders/1UTj1dcced5TFTttRLa4NIxYcJK4TjNPB?usp=drive_link)

* **Model pretrain**:

  [Tải model tại đây](https://drive.google.com/file/d/1kiDmf6XJZM99sJ01KNpCZ3x-qT2cuxmP/view?usp=drive_link)


---

## Thiết lập môi trường

```bash
# clone repo
git clone git@github.com:PhanDaiCuong/DSCT.git
cd DSCT

# tạo virtualenv / conda
conda create -n dsct python=3.10 -y
conda activate dsct
pip install -r requirements.txt
```

---

## Chuẩn bị dữ liệu

1. Tạo thư mục `dataset/` ở gốc repo.
2. Tải dataset từ `LINK` và đặt vào `dataset/`.

Ví dụ (wget):

```bash
mkdir -p dataset
wget -O dataset/data.zip "DATASET_LINK"
unzip dataset/data.zip -d dataset/
```

Nếu dùng Google Drive, bạn có thể dùng `gdown` hoặc script nhỏ để tải tự động.

---




## Liên hệ

* Email: `phancuongtmtlhp@gmail.com`

---

## License

MIT © 2025 Phan Đại Cương
