# CHARACTER DEVICE
## 1. Mở đầu

- công dụng: để có thể code kernel hay driver mà không cần quan tâm đến cấu trúc Hardware, là quy chuẩn chung để mọi dev code theo

Cây phân cấp Device Driver:
https://elixir.bootlin.com/linux/v6.5.9/source/drivers
  Tại đường link trên, trong thử mục Source/drivers/, có rất nhiều cây thư mục con, mỗi thư mục sẽ chứa các driver của module khác nhau, trong mỗi module như vậy sẽ chứa config cho từng hãng.