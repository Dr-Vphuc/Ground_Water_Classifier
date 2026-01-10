# Ground_Water_Classifier

## Thông tin thành viên

| **Họ tên**           | **Mã sinh viên** | **Tên GitHub**        | **Đóng góp**                          |
|----------------------|------------------|-----------------------|---------------------------------------|
| Nguyễn Việt Phúc     | 23001547         | Dr-Vphuc              | Tiền xử lí, phân cụm, K-NN             |
| Nguyễn Khắc Huy      | 23001525         | huynguyenkhac17       | Giảm chiều dữ liệu, GNB, MLP           |
| Trần Đăng Tài        | 23001558         | TaiTranDang145        | SoftMax, SVM                           |

## Hướng dẫn chạy chương trình

### Ưu tiên link colab notebook
Ưu tiên sử dụng link colab để tránh tải thư viện nặng, thầy/cô có thế làm theo các cách sau:

Truy cập trực tiếp từ link sau đây:
1. a_preprocessing : https://colab.research.google.com/drive/1iiz3bBtTjINEBLZ4ORB_eMctR06n1FFV
2. b_dimension_reduce : https://colab.research.google.com/drive/1-tADIbfK0VRyCgIIjBncFXLgKz_84Pqe
3. c_knn : https://colab.research.google.com/drive/17NpgiYM95V21xfLh9wJtIgZOhUPm-AAk
4. d_knn_with_lda : https://colab.research.google.com/drive/1pyvE-mrYlUPy0-nEtSu5RZLNcC37SbMZ
5. e_clustering : https://colab.research.google.com/drive/1luw5Hn-U0VJiJRLXImc1ABf8YIEwCUmr?usp=sharing
6. f_gnb+mlp-softmax : https://colab.research.google.com/drive/1m9qMtO3w_7RfSW_K2aeartrRzZ2bfsMI?usp=sharing
7. g_softmax : https://colab.research.google.com/drive/1zO4qwkN31rt0eXPNlpG-8mnwpgyY5RcJ
8. h_svm : https://colab.research.google.com/drive/15TOo4IqDeE9mCmwPyRnIS-z0inxSsoeX
9. i_svm_regression : https://colab.research.google.com/drive/1knsWz3ZFbCy-V7QFv_7kcFctjMiOisWq
10. k_softmax_regression : https://colab.research.google.com/drive/1_NT2W3ktPwoRBWHrwaxEu1PIa6a-6Nh_


### Jupyter notebook
Thầy/cô có thể sử dụng repo dự án của nhóm theo hướng dẫn sau:
1. cmd:
```cmd
git clone https://github.com/Dr-Vphuc/Ground_Water_Classifier.git
```
2. Làm theo [hướng dẫn lấy dữ liệu](#hướng-dẫn-tải-dữ-liệu)
3. Tạo venv nếu cần
4. pip install -r requirements.txt
5. Chạy dự án theo hướng dẫn trong phần [tổ chức dự án](#tổ-chức-dự-án)

## Hướng dẫn tải dữ liệu

Nếu thầy/cô kiểm tra mã nguồn bằng link colab notebook thì không cần quan tâm đến phần này.

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