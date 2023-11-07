# DEVICE TREE
> Đây là một khái niệm quan trọng mà mọi embedded linux dev nào cũng phải nắm rõ, để có thể tiến tới một quy chuẩn chung, hiểu rõ hơn về cách thức một hệ điều hành tác động lên phần cứng thiết bị.

## 1. Device tree là gì ?
Như mọi người đã biết, trong lập trình nói chung và lập trình embeddeded nói riêng, không có một quy chuẩn nào cho các dev để có một tiếng nói chung:
- Từ cách đặt tên biến:
  
![image](https://github.com/4ndykhang99/Hoc_Hanh_Cac_Kieu/assets/78153591/fb4178a8-11e3-4651-9306-1237e1e9d335)

cả 2 dòng define trên đều khai báo cho thanh ghi Set Data Out 0x194, nhưng mỗi người một cách đặt tên khác nhau, không thống nhất tên, có thể người đọc sẽ không hiểu tên biến đó đại diện cho phần tử nào.

- Không thống nhất về giá trị biến: thay vì offset từ giá trị 0x00 lên 0x04 đơn vị, thì người khác vẫn có thể offset từ 0x01 lên 0x03 đơn vị, hoặc đơn giản hơn, trong tìm nghiệm một phương trình bậc 2, có người khai báo giá trị là delta, có người khai báo là delta phẩy, tùy cách mỗi người tư duy mà giá trị biến họ khai báo cũng sẽ khác nhau.
- 
