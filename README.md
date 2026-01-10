# Ground_Water_Classifier

## Thông tin thành viên

| **Họ tên**           | **Mã sinh viên** | **Tên GitHub**        | **Đóng góp**                          |
|----------------------|------------------|-----------------------|---------------------------------------|
| Nguyễn Việt Phúc     | 23001547         | Dr-Vphuc              | Tiền xử lí, phân cụm, K-NN             |
| Nguyễn Khắc Huy      | 23001525         | huynguyenkhac17       | Giảm chiều dữ liệu, GNB, MLP           |
| Trần Đăng Tài        | 23001558         | TaiTranDang145        | SoftMax, SVM                           |

## Hướng dẫn chạy chương trình

Ưu tiên sử dụng link colab để tránh tải thư viện nặng, thầy/cô hãy chạy câu lệnh trong cmd/powershell để lấy link notebook:
- cmd: 
```cmd
curl https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/_presentation/link_colab.txt
```
-powershell:
```cmd
curl https://raw.githubusercontent.com/Dr-Vphuc/Ground_Water_Classifier/refs/heads/main/_presentation/link_colab.txt -UseBasicParsing | Select-Object -ExpandProperty Content
```

## Hướng dẫn tải dữ liệu

Trên window, sử dụng cmd (lưu ý là cmd chứ không phải powershell) di chuyển vào thư mục chứa dự án và chạy các lệnh sau:

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
Toàn bộ dữ liệu sẽ nằm trong folder <mark>\data</mark>, trong đó folder <mark>\raw</mark> chứa dữ liệu gốc và các files là các dữ liệu sau bước tiền xử lí.  

Nếu có bất kì vấn đề với bước trên, hãy tải theo [link backup](https://drive.google.com/drive/folders/1RA56Pm9FKjC0MQXaV6RFM1TUK-v8Fv_u?usp=sharing).  

## Tổ chức dự án

Toàn bộ mã nguồn của dự án được tổ chức bằng jupyter notebook trong thư mục <mark>\notebook</mark>.  
Thứ tự chạy các file là thứ tự của tên file (từ a -> k), tuy nhiên các file đều có thể chạy riêng lẻ vì đã được chuẩn bị dữ liệu processed đầy đủ.

Note: Có 2 file ghi dữ liệu là a_preprocessing.ipynbc và d_dimension_reduce.ipynb, thầy/cô có thể xóa các <mark>files</mark> trong folder <mark>\data</mark> (lưu ý phải để lại folder <mark>\raw</mark>) để kiểm chứng kết quả ghi file.