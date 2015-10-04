## Lý thuyết cơ bản
***Thế nào là lập trình hướng đối tượng?***

Lập trình hướng đối tượng là cách lập trình dựa trên sự tương tác các đối tượng. Một đối tượng bao gồm 2 thành phần chính là thông tin lưu trữ (thuộc tính) và các thao tác xử lý (phương thức).

***Ưu điểm, nhược điểm của lập trình hướng đối tượng?***

*Ưu điểm:*

* Dễ bảo trì, cập nhật
* Phát triển nhanh hơn, giảm giá thành phần mềm nhờ khả năng sử dụng lại code
* Code linh hoạt và đáng tin cậy hơn
* Code dễ hiểu hơn

*Nhược điểm:*

* Mất nhiều thời gian để tiếp cận hơn, nhiều khái niệm khó hiểu cho người mới học
* Size của project sẽ lớn hơn: có thể phải viết nhiều code hơn so với lập trình hướng thủ tục
* Chương trình chậm hơn: vì có nhiếu phép toán được thực thi hơn


***Các đặc điểm của lập trình hướng đối tượng***

* *Tính trừu tượng (abstraction):* là kĩ thuật chỉ trình bày những đặc điểm cần thiết của vấn đề mà không trình bày những chi tiết cụ thể hay những lời giải thích phức tạp của vấn đề đó. Nói cách khác là một kĩ thuật tập trung vào những thứ cần thiết và phớt lờ đi những thứ không cần thiết.

* *Tính bao đóng (encapsulation):* Là khả năng che dấu thông tin của đối tượng, hay nói cách khác là khả năng kiểm soát các thao tác từ bên ngoài, tính chất này đảm bảo tính toàn vẹn của đối tượng.

* *Tính kế thừa (inheritance):* Là khả năng cho phép ta xây dựng một lớp mới dựa trên các định nghĩa của một lớp đã có sẵn, lớp mới là lớp lớp con, lớp có sẵn là lớp cha, lớp con sẽ kế thừa các thành phần của lớp cha, lớp con có thể mở rộng các thành phần của lớp cha và có thể bổ sung thêm các thành phần mới

* *Tính đa hình (polymorphism):* là khả năng thực hiện một hành động bằng nhiều cách khác nhau.

***Nạp chồng (overloading), ghi đè (overriding)***

* *Nạp chồng (overloading):* là khả năng cho phép một lớp có nhiều thuộc tính, phương thức có cùng tên nhưng với các tham số khác nhau về loại cũng như về số lượng. Khi được gọi, dựa vào tham số truyền vào, phương thức sẽ được thực hiện tương ứng.

* *Ghi đè (overriding):* là khả năng cho phép cài đặt lại một phương thức của lớp con từ lớp cha.

* *Sự khác nhau giữa overloading và overriding:* 

***Thế nào là abstract class, interface, so sánh sự khác nhau giữa 2 khái niệm?***

* *Abstract class:* có thể hiểu là một class cha cho tất cả các class con có cùng bản chất. Do đó, mỗi lớp con chỉ có thể kế thừa từ một lớp trừu tượng. Abstract class không cho phép tạo các thể hiện, vì vậy không thể tạo một đối tượng trực tiếp từ một abstract class.

* *Interface:* Interface có thể được xem là một mặt nạ cho tất cả các class có cùng cách thức hoạt động nhưng có thể khác nhau về bản chất. Từ đó một lớp con có thể kế thừa từ nhiều interface khác nhau để bổ sung đầy đủ cách thức hoạt động của mình (đa kế thừa).

* *Sự khác nhau:*

 * Abstract class có thể chứa các phương thức được cài đặt hoặc các biến, hằng có giá trị, còn interface thì không.

 * Phương thức của abstract class có thể sử dụng access modifiers như private, public, protected. Interface mặc định là public và abstract

 * Lớp con của abstract class chỉ cần định nghĩa lại những phương thức abstract, còn class implement interface thì phải định nghĩa tất cả các phương thức của interface

 * Một lớp con của abstract class chỉ được kế thừa một lớp cha trừu tượng, còn một lớp con có thể implement nhiều interface cùng một lúc.

 * Abstract class có thể kế thừ từ class khác và implement nhiều interface, còn interface thì chỉ có thể implement nhiều interface

## Các khái niệm

***Khái niệm lớp, đối tượng?***

* *Đối tượng:* là mọi thứ có thể nhìn thấy xung quanh ta, đối tượng có trạng thái và hành vi.

* *Lớp:* là khuân mẫu mô tả trạng thái, hành vi của đối tượng.

***Static field, static method?***

* *Static field:* thuộc tính tĩnh là thuộc tính mang tính toàn cục của class, nghĩa là giá trị của thuộc tính đó không phụ thuộc vào từng đối tượng riêng lẻ của class đó.

* *Static method:* Phương thức tĩnh là phương thức không phụ thuộc vào đối tượng của class. Nó có thể gọi trực tiếp mà không cần phải tạo đối tượng của class

* *Ưu điểm:* Có thể dùng mà không cần phải tọa đối tượng của class => tiết kiệm bộ nhớ hơn

* *Nhược điểm:* Chỉ truy xuất được đến các thuộc tính, phương thức tĩnh

***Final keyword***

*Class final:* là lớp không thể kế thừa

*Variable final:* là biến không thể thay đổi giá trị => trờ thành hằng số

*Method final:* là phương thức không thể ghi đè

***Constructor & Destructor***

* *Constructor:* là phương thức khởi tạo trạng thái của đối tượng, nó được gọi khi đối tượng được khởi tạo.

* *Destructor:* là phương thức được tự động gọi khi đối tượng hủy