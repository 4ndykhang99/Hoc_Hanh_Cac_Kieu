# PROCESS MANAGEMENT
>Chương này sẽ giới thiệu về khái niệm của tiến trình (process). Bộ quản lý tiến trình là một yếu tố cốt lõi của bất kì hệ điều hành nào, trong đó có cả Linux.
## PROCESS LÀ GÌ ?
Tiền trình là một chương trình (object code stored on some media) . Bên cạnh việc thi hành đoạn mã chương trình (text section in Unix), các tiến trình còn bao gồm:

- Mở các file.
- Chờ các tín hiệu.
- Dữ liệu bên trong kernel.
- Trạng thái bộ xử lý.
- Không gian địa chỉ trong bộ nhớ (with one or more memory mappings).
- Các thread.
- Vùng dữ liệu chứa biến toàn cục.

## THREAD LÀ GÌ ?

>Các thread là các hoạt động bên trong một tiến trình. Mỗi thread chứa:

- Bộ đếm chương trình (program counter).
- Ngăn nhớ tiến trình (process stack).
- Tập các thanh ghi bộ xử lý.

>Kernel lập lịch cho các thread, chứ không phải là các tiến trình (process). Linux không phân biệt giữa thread và process. Với Linux, một thread là một loại tiến trình đặc biệt.

## SƠ BỘ TỔ CHỨC HOẠT ĐỘNG CỦA TIẾN TRÌNH TRÊN LINUX

Như mọi người có thể thấy, trong Task Manager của Window, có rất nhiều process đang chạy:

![image](https://github.com/4ndykhang99/Hoc_Hanh_Cac_Kieu/assets/78153591/163c76e7-a4df-42c1-b382-e8ae265fcd98)

Câu hỏi đặt ra: làm thế nào để máy tính có thể nhận biết được có những tiến trình nào đang hoạt động, tiến trình đó sử bao nhiêu tài nguyên của máy tính bao gồm CPU, RAM, DISK, NETWORK,...

=> Tiến trình là một khái niệm trừu tường, được thực thể hóa qua các tệp (file), các tệp này sẽ bao hàm các thông tin như
