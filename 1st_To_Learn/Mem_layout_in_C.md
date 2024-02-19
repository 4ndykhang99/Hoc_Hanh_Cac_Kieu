## MEMORY LAYOUT IN C PROGRAMMING
### 1. Tiếp cận vấn đề

Thông thường, khi thực hiện một dự án lập trình embedded C, chúng ta sẽ thực hiện các trình tự sau:
- Viết, chỉnh sửa code file (C/Cpp) -> Chương trình được lưu trong ổ cứng.
- Biên dịch (compile chương trình) sang ngôn ngữ máy tính (Binary file) -> binary file cũng được lưu trong ổ cứng.
- Chạy chương trình -> Load chương trình vào bộ nhớ của vi xử lý

### 2. Layout của một memory trong ngôn ngữ C
![image](https://github.com/4ndykhang99/Hoc_Hanh_Cac_Kieu/assets/78153591/6361e835-2341-43ed-af79-c8df199c2016)

### a. Text segment

> Đây là vùng nhớ chứa mã máy đã được biên dịch của chương trình. Nó chứa các hàm, lệnh điều khiển và các phần mã khác. khu vực này được định dạng read only để ngăn chặn truy cập chỉnh sửa trái phép từ bên ngoài.

### b. DS - Data segment - initialized data segment
> Có thể hiểu vùng bộ nhớ này chứa các biến đã được khai báo với giá trị khác 0

eg:

```c
#include <stdio.h>

// Khai báo biến toàn cục trong vùng DS
int global_variable = 10;


int main() {
    // Khai báo biến cục bộ trong vùng DS
    int local_variable = 20;

    // In giá trị của các biến
    printf("Global variable: %d\n", global_variable);
    printf("Local variable: %d\n", local_variable);

    return 0;
}
```
### c. BSS - Block Started by Symbol
> Đây là vùng nhớ chứa các biến chỉ được khai báo nhưng chưa gán giá trị hoặc có giá trị bằng 0

eg:
Dưới đây là một ví dụ về cách khai báo và sử dụng vùng nhớ BSS trong C:

```c
#include <stdio.h>

// Khai báo một biến và mảng toàn cục trong vùng BSS
int uninitialized_array[100];
int A = 0;
int main() {
    // In giá trị của phần tử đầu tiên trong mảng
    printf("Uninitialized array element: %d\n", uninitialized_array[0]);

    // Gán giá trị cho phần tử đầu tiên trong mảng
    uninitialized_array[0] = 42;

    // In giá trị đã gán cho phần tử đầu tiên trong mảng
    printf("Updated array element: %d\n", uninitialized_array[0]);

    return 0;
}
```

