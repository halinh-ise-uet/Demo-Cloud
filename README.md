# SPRING BOOT Demo on Google App Engine - Google Cloud Platform
Đây là dự án demo triển khai một ứng dụng Spring Boot đơn giản trên Google App Engine (môi trường chuẩn) sử dụng Google Cloud Platform (GCP) Free Trial. Ứng dụng triển khai demo một trang html đơn giản. 
Dự án được thiết kế để: 

# URL triển khai mẫu: 
```https://plasma-crossbar-456903-e3.as.r.appspot.com ```
Note: chỉ hoạt động trong thời gian Free Trial hoặc nếu dự án vẫn tồn tại.

# Chi tiết quá trình 
### Cấu trúc dự án: 
![image](https://github.com/user-attachments/assets/f04ed85b-72fc-42e4-9a24-f47bd43ed02d)


### Cài đặt 
###### Khởi tạo Google Cloud  
``` gcloud init ```

###### Khởi tạo App Engine 
```gcloud app create --project=plasma-crossbar-456903-e3 ```
- Ở đây, ` plasma-crossbar-456903-e3 ` là Project ID

###### Triển khai lên Google App Engine 
- Cấp quyền cho tài khoản dịch vụ
  ```
  gcloud projects add-iam-policy-binding plasma-crossbar-456903-e3 \
    --member=serviceAccount:plasma-crossbar-456903-e3@appspot.gserviceaccount.com \
    --role=roles/storage.admin
  ```
- Triển khai
  ```
  mvn clean package appengine:deploy
  ```
- Truy cập URL
  ```
  gcloud app browse
  ```

  # DEMO
  #### Chạy cục bộ
  ![image](https://github.com/user-attachments/assets/3952695c-d2b3-4c38-a857-818023ebb0b4)

  #### Google Cloud
  ![image](https://github.com/user-attachments/assets/a5cc922b-2b2f-4085-8363-370375dfca22)

  ###### URL Thử nghiệm:
  ```https://plasma-crossbar-456903-e3.as.r.appspot.com ```
