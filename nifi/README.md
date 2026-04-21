# NiFi Template

Template triển khai **Apache NiFi** để chạy local bằng Docker Compose.

## Cấu trúc thư mục

```text
.
├── docker-compose.yaml
├── Dockerfile
└── README.md
```

## Yêu cầu

- Docker
- Docker Compose

## Cài đặt

### 1. Khởi động dịch vụ

```bash
docker compose up -d --build
```

### 2. Truy cập NiFi UI

Mở trình duyệt tại:

```text
https://localhost:9443
```

### 3. Đăng nhập

- Username: `admin`
- Password: `Admin@12345678`

## Một số lệnh hữu ích

### Xem logs

```bash
docker compose logs -f nifi
```

### Xem log cleaner

```bash
docker compose logs -f nifi-log-cleaner
```

### Dừng dịch vụ

```bash
docker compose down
```

### Dừng và xóa containers

```bash
docker compose down -v
```

## Lưu ý

- NiFi chạy qua HTTPS nên truy cập bằng `https://localhost:9443`
- Trình duyệt có thể cảnh báo chứng chỉ self-signed, chọn tiếp tục để vào UI
- Nếu không cần network `lakehouse`, có thể bỏ phần `networks`
- Dữ liệu NiFi được lưu trong thư mục `./nifi_data`
