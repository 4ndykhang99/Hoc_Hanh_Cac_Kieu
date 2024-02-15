# EMBEDDED INTERVIEW
## 1. Introduce yourself
- Name, Education, Major:

  - Hi, my name is Khang, I graduated from CanTho University with a bachelor's in Mechatronics, I finished my education at the end of 2021, and have worked for MyLanGroup till now as an R&D technician.
Experiences at workplaces

- Achievement ( what - When ) - Skill (3)

  - In my first year at Mylan, I worked on electrical design and PLC programming. However, I realized that it wasn't aligned with my career path. Therefore, I requested to switch to hardware design and firmware programming, which better matched my interests. I gained one year of experience in those fields and completed two projects for Mylan.
  
  - Today, I'm here to explore new opportunities and advance my career.

  - I hope we will have a productive interview today.
  
Extra Activities : scopus article - badminton 
=> From these things, I will contribute my value to your organization!
## 2. Strength - weakness
### a. Weakness
- Weakness -> Improvement : detailed -> waste time -> after 2 machines, I improve almost

### b. Strength

- Strength: I have noticed three strong points in myself:
  
  - Firstly, I am a person who is willing to learn and open to receiving feedback to understand my areas for improvement.
  - Secondly, I am a fast learner, which allows me to approach tasks rapidly and efficiently Lastly, 

## 3. Why did you quit your job?

- Simply, My current job does not match my career path which I am applying for.

  -> I prefer the international, dynamic, and challenging environment like FPT 

  -> To be honest, I do expect to win the position of Senior …., but it requires more qualifications than I do, so I decided to start with this position first with my willingness to learn and contribute. 

## 4. Long-term and short-term goals

  -> My short-term goal is to be a master in this position ASAP, for at least 2 years. 

  -> Long term 5 years: challenge me to accumulate knowledge as much as possible to  be a Senior Coder …
  
## V. Why did you choose our company? 

  -> Corporate culture -> 
  -> FPT is a famous company.
  -> Shorter distance to go to hometown

## 5. Salary 

- The average salary range for this position in such a professional company like yours  is from A to B. I am satisfied to dedicate all of the value and stable with any hesitation, I expect my salary at … 

## 6. Tell me the reason why I choose you.

- willing to listen and learn 
- persistent

## 7. What do you expect anything from my company/ this position?
- Training course in knowledge and skill 

- A clear proficiency pathway

- Knowledge and skill training & testing

## 8. Question to ask them? 
- Benefit


# C PROGRAMMING AND EMBEDDED QUESTION
## 1. Các kiểu dữ liệu của biến - size của từng kiểu dữ liệu ?
- Kiểu int:
kích thước 2 - 4 bytes tùy  người dùng khai báo
định dạng %d, %i

- Kiểu float và double:
float: 4 bytes
Double: 8 bytes
Định dạng: %f, %lf

- Kiểu Char:
kích thước: 1 byte
định dạng: %c

- Short và Long:
Short: 2 bytes
Long: 4 đến 8 bytes

- Bool:
Kích thước: 1 byte

## 2. Volatile, static, inline, extern.
- Volatile:
  - Định nghĩa: Volatile là một từ khóa được sử dụng để chỉ rằng biến có thể thay đổi bất kỳ lúc nào bởi các yếu tố bên ngoài (ví dụ: ngắt, thiết bị phần cứng).
  - Ưu điểm:
    -Đảm bảo rằng trạng thái của biến luôn được cập nhật chính xác.
    -Hữu ích trong việc làm việc với các biến liên quan đến ngắt hoặc thiết bị ngoại vi.
  -Nhược điểm:
    -Có thể làm tăng độ phức tạp của mã nguồn.
    -Không phù hợp cho tất cả các biến.
- Static:
  - Định nghĩa: Static là một từ khóa được sử dụng để chỉ rằng biến hoặc hàm chỉ có phạm vi trong cùng một tệp nguồn.
  - Ưu điểm:
    - Biến static không bị xung đột với các biến cùng tên trong các tệp nguồn khác.
    - Hàm static không thể gọi từ bên ngoài tệp nguồn.
  - Nhược điểm:
    - Không thể truy cập từ các tệp nguồn khác.
    - Có thể làm tăng kích thước của tệp thực thi.
- Inline:
  - Định nghĩa: Inline là một từ khóa được sử dụng để yêu cầu trình biên dịch thực hiện việc nhúng mã của hàm trực tiếp vào nơi gọi hàm.
  - Ưu điểm:
    - Tối ưu hóa hiệu suất bằng cách tránh gọi hàm.
    - Giảm thời gian gọi hàm.
  - Nhược điểm:
    - Tăng kích thước của mã thực thi.
    - Không phù hợp cho các hàm lớn hoặc phức tạp.
- Extern:
  - Định nghĩa: Extern là một từ khóa được sử dụng để khai báo biến hoặc hàm đã được định nghĩa ở nơi khác.
  - Ưu điểm:
    - Cho phép sử dụng biến hoặc hàm từ các tệp nguồn khác.
    - Hữu ích trong việc chia sẻ mã nguồn giữa các tệp.
  - Nhược điểm:
    - Cần phải đảm bảo rằng biến hoặc hàm đã được định nghĩa ở nơi khác.
    - Có thể gây xung đột tên biến hoặc hàm.
## 3. Pointer
> Con trỏ là một biến đặc biệt trong một số ngôn ngữ lập trình, thường được sử dụng để lưu trữ địa chỉ bộ nhớ của một biến khác. Con trỏ cho phép chúng ta truy cập và thay đổi giá trị của biến được trỏ tới thông qua việc tham chiếu đến địa chỉ bộ nhớ.

- Con trỏ: Con trỏ là một biến chứa địa chỉ bộ nhớ của một biến khác.
  - Để khai báo con trỏ, chúng ta sử dụng dấu * trước tên biến. Ví dụ: int* ptr;.
  - Để lấy địa chỉ của một biến, chúng ta sử dụng toán tử &. Ví dụ:
    ```int num = 10; int* ptr = &num;.```
  - Để truy cập giá trị của biến được trỏ tới, chúng ta sử dụng toán tử * trước con trỏ. Ví dụ: int value = *ptr;.

- Con trỏ hàm: Con trỏ hàm là một biến chứa địa chỉ của một hàm.
  - Để khai báo con trỏ hàm, chúng ta sử dụng cú pháp tương tự như khai báo con trỏ, nhưng với kiểu dữ liệu là kiểu chữ ký của hàm. Ví dụ: int (*funcPtr)(int, int);.
  - Để gán con trỏ hàm cho một hàm cụ thể, chúng ta chỉ cần sử dụng tên hàm. Ví dụ: funcPtr = sum;.
  - Để gọi hàm thông qua con trỏ hàm, chúng ta sử dụng cú pháp tương tự như gọi hàm trực tiếp. Ví dụ: int result = (*funcPtr)(a, b); hoặc int result = funcPtr(a, b);.

- Con trỏ hằng và hằng con trỏ:
  - Con trỏ hằng (const pointer): Một con trỏ hằng không thể thay đổi địa chỉ mà nó trỏ tới. Ví dụ: int* const ptr = &num;.
  - Hằng con trỏ (pointer to constant): Một hằng con trỏ không thể thay đổi giá trị của biến được trỏ tới. Ví dụ: const int* ptr = &num; hoặc int const* ptr = &num;.
