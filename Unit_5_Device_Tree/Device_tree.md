# DEVICE TREE
> Đây là một khái niệm quan trọng mà mọi embedded linux dev nào cũng phải nắm rõ, để có thể tiến tới một quy chuẩn chung, hiểu rõ hơn về cách thức một hệ điều hành tác động lên phần cứng thiết bị.

## 1. Device tree là gì ?
Như mọi người đã biết, trong lập trình nói chung và lập trình embedded nói riêng, không có một quy chuẩn nào cho các dev để có một tiếng nói chung:
- Từ cách đặt tên biến:
```
  #define GPIO_SET_DATA_OUT 0x194;
  #define GPIO_SDTO 0x194;
```

Cả 2 dòng define trên đều khai báo cho thanh ghi ```Set Data Out 0x194```, nhưng mỗi người một cách đặt tên khác nhau, không thống nhất tên, có thể người đọc sẽ không hiểu tên biến đó đại diện cho phần tử nào.

- Không thống nhất về giá trị biến: thay vì offset từ giá trị 0x00 lên 0x04 đơn vị, thì người khác vẫn có thể offset từ 0x01 lên 0x03 đơn vị, hoặc đơn giản hơn, trong tìm nghiệm một phương trình bậc 2, có người khai báo giá trị là delta, có người khai báo là delta phẩy, tùy cách mỗi người tư duy mà giá trị biến họ khai báo cũng sẽ khác nhau.

![image](https://github.com/4ndykhang99/Hoc_Hanh_Cac_Kieu/assets/78153591/3f96ee47-2456-4b95-aaa5-de18a0d2e68b)
  
Cấu trúc phần cứng của các thiết bị ngày càng phức tạp:
- Ví dụ như board beaglebone có nhiều dòng, mỗi dòng lại có nhiều module, để có thể cấu hình cho một phần cứng, để có thể giao tiếp giữa 2 board với nhau, programmer phải đọc tài liệu phần cứng của 2 board, so sánh điểm khác nhau và viết chương trình đọc ghi theo cấu trúc của ở cả 2 board.

==> Vì thế device tree được sinh ra để giải quyết các vấn đề trên.
- Device tree có các công dụng chính sau đây:
> Mô tả phần cứng: Device Tree được sử dụng để mô tả cấu trúc và thông tin về phần cứng của một hệ thống nhúng. Nó bao gồm các thông tin về vi xử lý (CPU), bộ nhớ, bộ điều khiển, các giao diện như I2C, SPI, UART, các thiết bị ngoại vi và các thành phần phần cứng khác. Device Tree giúp hệ điều hành Linux hiểu và tương tác với các thiết bị phần cứng này mà không cần biết trước về chúng.

> Độc lập phần cứng - phần mềm: Device Tree giúp tạo ra một giao diện trừu tượng giữa phần cứng và phần mềm. Nó cho phép phần mềm (như hạt nhân Linux) có thể được biên dịch và cấu hình trước, độc lập với phần cứng cụ thể. Điều này giúp tăng tính di động và khả năng tái sử dụng của phần mềm.

> Hỗ trợ nhiều nền tảng: Device Tree cho phép việc chuyển đổi và hỗ trợ nhiều nền tảng phần cứng khác nhau mà không cần viết lại hoàn toàn mã nguồn của hạt nhân Linux. Thay vì phải thay đổi mã nguồn, chỉ cần cung cấp một Device Tree phù hợp cho từng nền tảng.

> Điều chỉnh cấu hình phần cứng: Device Tree cung cấp một cách linh hoạt để điều chỉnh cấu hình phần cứng. Bằng cách chỉnh sửa hoặc thay đổi Device Tree, ta có thể thay đổi cấu hình phần cứng mà không cần sửa đổi mã nguồn của hạt nhân Linux.

> Hỗ trợ khả năng cấu hình động: Device Tree cho phép khả năng cấu hình động trong quá trình chạy. Điều này cho phép thêm hoặc xóa các thiết bị phần cứng mà không cần khởi động lại hệ thống.
