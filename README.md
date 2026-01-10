# Ground_Water_Classifier

## Thông tin thành viên

| **Họ tên**           | **Mã sinh viên** | **Tên GitHub**        | **Đóng góp**                          |
|----------------------|------------------|-----------------------|---------------------------------------|
| Nguyễn Việt Phúc     | 23001547         | Dr-Vphuc              | Tiền xử lí, phân cụm, K-NN             |
| Nguyễn Khắc Huy      | 23001525         | huynguyenkhac17       | Giảm chiều dữ liệu, GNB, MLP           |
| Trần Đăng Tài        | 23001558         | TaiTranDang145        | SoftMax, SVM                           |

## Hướng dẫn tải dữ liệu

Trên window, sử dụng cmd (lưu ý là cmd chứ không phải powershell) cd vào thư mục chứa dự án và chạy các lệnh sau:

```cmd
mkdir data
mkdir data\raw

curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/raw/ground_water_quality_2018_post.csv -o data\raw\ground_water_quality_2018_post.csv
curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/raw/ground_water_quality_2019_post.csv -o data\raw\ground_water_quality_2019_post.csv
curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/raw/ground_water_quality_2020_post.csv -o data\raw\ground_water_quality_2020_post.csv

curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/X_4_classes_LDA_2dims.csv -o data\X_4_classes_LDA_2dims.csv
curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/X_4_classes_PCA_6dims.csv -o data\X_4_classes_PCA_6dims.csv
curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/X_9_classes_LDA_2dims.csv -o data\X_9_classes_LDA_2dims.csv
curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/X_9_classes_PCA_6dims.csv -o data\X_9_classes_PCA_6dims.csv

curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/processed_data_4_classes.csv -o data\processed_data_4_classes.csv
curl -L https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/data/processed_data_9_classes.csv -o data\processed_data_9_classes.csv

```