# Secure File Transfer - Ký và Xác Thực File với RSA

Ứng dụng web Flask cho phép bạn:
- Tạo cặp khóa RSA (private/public)
- Ký số file bằng khóa riêng
- Xác thực chữ ký số file bằng khóa công khai

## Yêu cầu

- Python 3.7+
- pip

## Cài đặt

1. **Clone dự án:**
   ```
   git clone <link-repo>
   cd secure_file_transfer
   ```

2. **Cài đặt thư viện:**
   ```
   pip install flask cryptography
   ```

## Chạy ứng dụng

```
python app.py
```

Mặc định ứng dụng chạy trên: [http://127.0.0.1:5000](http://127.0.0.1:5000)

## Chức năng

- **Tạo cặp khóa RSA:**  
  Nhấn nút "Tạo & tải về cặp khóa RSA" để tải về file zip chứa private_key.pem và public_key.pem.

- **Ký file:**  
  Chọn "Ký file", upload file cần ký. Ứng dụng trả về file chữ ký `.sig`.

- **Xác thực chữ ký:**  
  Truy cập `/verify` hoặc tạo thêm nút trên giao diện, upload file gốc, file chữ ký và public key để kiểm tra tính hợp lệ.

## Cấu trúc thư mục

```
.
├── app.py
├── keys/
├── uploads/
├── templates/
│   ├── index.html
│   ├── sign.html
│   └── verify.html
```

## Lưu ý bảo mật

- Không chia sẻ private_key.pem cho bất kỳ ai.
- Chỉ sử dụng public_key.pem để xác thực chữ ký.

![image](https://github.com/user-attachments/assets/1d51c969-365c-4dfc-a1dc-49ba45fbf09d)

# Secure File Transfer - Xác Thực File An Toàn

Đây là một ứng dụng web Flask giúp bạn **xác minh chữ ký số** của file, đảm bảo file không bị chỉnh sửa và xác thực nguồn gốc file thông qua public key.

## Tính năng

- Tạo cặp khóa RSA (private & public key)
- Ký file bằng private key và sinh file chữ ký `.sig`
- Xác minh file với chữ ký và public key
- Giao diện hiện đại, dễ sử dụng, hỗ trợ tiếng Việt

## Yêu cầu

- Python 3.7+
- pip

## Cài đặt

1. **Clone dự án:**
    ```bash
    git clone <repo-url>
    cd secure_file_transfer
    ```

2. **Cài đặt thư viện:**
    ```bash
    pip install -r requirements.txt
    ```
    > Nếu chưa có file `requirements.txt`, cài đặt thủ công:
    ```bash
    pip install flask cryptography
    ```

3. **Chạy ứng dụng:**
    ```bash
    python app.py
    ```

4. **Truy cập trình duyệt:**  
   Mở [http://127.0.0.1:5000](http://127.0.0.1:5000)

## Hướng dẫn sử dụng

### 1. Tạo cặp khóa RSA
- (Nếu chưa có) Nhấn nút tạo khóa để tải về file `private_key.pem` và `public_key.pem`.

### 2. Ký file
- Chọn file cần ký, hệ thống sẽ trả về file chữ ký `.sig`.

### 3. Xác minh chữ ký
- Chọn file gốc, file chữ ký `.sig` và public key `.pem`.
- Hệ thống sẽ thông báo kết quả xác minh.

## Cấu trúc thư mục

```
secure_file_transfer/
│
├── app.py
├── keys/
├── uploads/
├── templates/
│   ├── index.html
│   ├── sign.html
│   ├── verify.html
│   └── result.html
└── requirements.txt
```

## Công nghệ sử dụng

- Python Flask
- cryptography (thư viện mã hóa)
- Bootstrap 4, Animate.css, FontAwesome (giao diện)

## Ghi chú bảo mật

- **Không chia sẻ private key cho bất kỳ ai!**
- File upload chỉ lưu tạm thời, nên xóa sau khi sử dụng nếu triển khai thực tế.

![image](https://github.com/user-attachments/assets/4b8ff821-5842-4deb-b3ac-11693e8da1d3)


**Tác giả:**  
- [Dương Huy Hoàng - CNTT 17-07]  
- 2025

