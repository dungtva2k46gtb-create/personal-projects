# n8n Template

Template triển khai **n8n** để chạy local bằng Docker Compose.

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

### 2. Truy cập n8n UI

Mở trình duyệt tại:

```text
http://localhost:5678
```


## Một số lệnh hữu ích

### Xem logs

```bash
docker compose logs -f n8n
```

### Dừng dịch vụ

```bash
docker compose down
```

### Dừng và xóa dữ liệu volume

```bash
docker compose down -v
```

## Lưu ý

- Chạy local thì dùng `localhost` cho `N8N_HOST` và `WEBHOOK_URL`
- Nếu webhook cần gọi từ máy khác, hãy thay `localhost` bằng IP hoặc domain thật
- Nếu có `Dockerfile`, dùng `docker compose up -d --build` để build lại image khi cần
