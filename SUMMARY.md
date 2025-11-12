
---

## 📈 Quy trình huấn luyện & dự đoán
1. **Chuẩn bị dữ liệu:**
   - Lấy dữ liệu cổ phiếu (VD: `GEX`, `DPM`, …)
   - Tính toán các chỉ báo kỹ thuật: SMA, Bollinger Bands, STD, v.v.

2. **Xây dựng mô hình LSTM:**
   - Sử dụng `window_size = 60`
   - Các layer: `LSTM`, `Dropout`, `Dense`
   - Huấn luyện với **EarlyStopping** và **ModelCheckpoint**

3. **Đánh giá mô hình:**
   - Metrics: MAPE, MAE, MSE, RMSE, R²
   - Vẽ biểu đồ: Train vs Validation Loss, Actual vs Predicted

4. **Dự đoán tương lai:**
   - Tạo cửa sổ 60 ngày gần nhất
   - Dự báo giá Close 30 ngày kế tiếp
   - Xuất biểu đồ dự đoán và file kết quả

---

## 🧩 Cài đặt
```bash
# Clone project
git clone https://github.com/Biglucky-DA/Predict-Future-Model.git
cd Predict-Future-Model

# Tạo môi trường ảo (tuỳ chọn)
python -m venv .venv
source .venv/bin/activate  # (hoặc .venv\Scripts\activate trên Windows)

# Cài thư viện
pip install -r requirements.txt
