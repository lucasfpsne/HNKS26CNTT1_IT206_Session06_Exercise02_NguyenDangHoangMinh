# Khắc phục lỗi khai báo biến số trong prompt mẫu

## Bước 1. Phân tích lỗi

Prompt cũ dùng ngoặc vuông cho `[language]` và ngoặc nhọn cho `{audience}`. Nếu công cụ tự động chỉ tìm biến trong ngoặc vuông, nó sẽ thay `[language]` nhưng bỏ sót `{audience}`. Khi đó, AI biết phải viết bằng ngôn ngữ nào nhưng thiếu thông tin về người đọc.

## Bước 2. Prompt đã đồng bộ biến số

```text
Hãy viết một bài chia sẻ ngắn về ứng dụng AI trong học tập và nghiên cứu bằng [NGÔN_NGỮ], dành cho [ĐỐI_TƯỢNG]. Nêu một ví dụ về cách dùng AI khi học và một ví dụ khi đọc tài liệu nghiên cứu.
```

## Bước 3. Chạy thử với dữ liệu thực tế

| Biến | Giá trị thay thế |
|---|---|
| `[NGÔN_NGỮ]` | tiếng Việt |
| `[ĐỐI_TƯỢNG]` | sinh viên năm nhất ngành Công nghệ thông tin tại PTIT |

### Prompt sau khi điền

> Hãy viết một bài chia sẻ ngắn về ứng dụng AI trong học tập và nghiên cứu bằng tiếng Việt, dành cho sinh viên năm nhất ngành Công nghệ thông tin tại PTIT. Nêu một ví dụ về cách dùng AI khi học và một ví dụ khi đọc tài liệu nghiên cứu.

### Kết quả chạy thử

Khi mới học lập trình C, bạn có thể nhờ AI đưa ra một vòng lặp ngắn rồi tự đoán kết quả trước khi chạy chương trình. Nếu đoán sai, hãy nhờ AI giải thích giá trị của biến sau mỗi lần lặp để tìm ra bước mình hiểu nhầm.

Khi đọc một bài nghiên cứu, bạn có thể gửi phần tóm tắt cho AI và hỏi “Tác giả muốn giải quyết vấn đề gì?”. Sau đó, hãy đọc phần kết quả trong bài gốc để kiểm tra xem số liệu nào thực sự ủng hộ kết luận của tác giả.
