### Thế nào là design pattern?

Design pattern cũng cấp các mẫu thiết kế, giải pháp để giải quyết các vấn đề chung, hay gặp trong lập trình.

Design pattern cung cấp giải pháp ở dạng tổng quát giúp tăng tốc phát triển phần mềm bằng cách đưa các mô hình test, mô hình phát triển đã qua kiểm nghiệm. Dùng lại các design pattern giúp tránh được các vấn đề tiềm ẩn có thể gây ra những lỗi lớn, dễ dàng nâng cấp, bảo trì về sau.

Sử dụng design pattern giúp các lập trình viên khác dễ dàng hiểu code của mình viết.

Design pattern giúp cho chương trình đơn giản, giúp chúng ta giảm được thời gian phát triển các vấn đề chung đã có lời giải.

Để hiểu và làm được design patterns, người lập trình cần phải nắm vứng 4 nguyên lý của lập trình hướng đối tượng: Thừa kế, đa hình, trừu tượng, bao đóng. Và 2 khái niệm abstract và interface.

Interface là trái tim của design pattern, nghĩa là mọi thứ trong design pattern đều phải sử dụng interface.

### Một số pattern phổ biến

1. **Singleton**
	
	`Singleton` là pattern đảm bảo việc một ứng dụng trong một thời điểm chỉ được phép có duy nhất một thể hiện của đối tượng `Singleton`. Có nghĩa là việc khởi tạo đối tượng chỉ duy nhất một lần đầu tiên, các lần sau, nó không được khởi tạo mới mà chính là đối tượng cũ. Điều này giúp tiết kiệm bộ nhớ và ngăn chặn việc tạo ra nhiều lần khởi tạo đối tượng.
	
	`Singleton` sử dụng khi trong ứng dụng có những thực thể bị truy xuất nhiều lần nhưng không cần thiết phải khởi tạo lại.
	
	Ví dụ: `Database connect`: nếu không dùng `Singleton`, mỗi lần muốn thao tác với db, chúng ta cần khởi tạo lại lớp `Database`.
1. **Observer**

	`Observer` cho phép các đối tượng có thể lắng nghe và phản ứng khi có thông báo từ một đối tượng khác. Tức là khi một đối tượng gửi thông báo, các đối tượng lắng nghe có thể phản ứng lại với thông báo đó.
	
1. **Decorator**

	Là việc bổ sung trách nhiệm cho đối tượng tại thời điểm thực thi. Đây được xem là sự thay thế hiệu qua cho phương pháp kế thừa trong việc bổ sung trách nhiệm cho đối tượng và mức tác động là ở mức đối tượng thay vì ở mức lớp như phương pháp kế thừa.
	
	Decorator pattern hoạt động dựa trên nguyên lý `Open/Closed`luôn mở cho việc mở rộng, nhưng đóng cho việc sửa đổi
	
	Ví dụ: Một đối tượng máy tính, tại một thời điểm có thể được add thêm ổ đĩa CD, ổ đĩa cứng, hoặc ổ đĩa mềm

1. **Factory**

	`Factory pattern` là việc định nghĩa một giao diện để tạo đối tượng, nhưng cho phép các lớp con quyết định cách thức thể hiện nó.
	
	Ví dụ: `ConnectionFactory` là một class để tạo đối tượng kết nối database, nhưng các lớp con như OracleConnection, MySqlConnection... mới là lớp quyết định cách thức thể hiện nó.
	

1. **Strategy**

	`Strategy` là pattern định nghĩa một tập hợp các thuật toán, đóng gói chúng thành từng loại một vaf lựa chọn thuật toán nào mà bạn cảm thấy đúng đắn và hợp lý nhất khi thực thi chương trình.
	
	Nên sử dụng `Strategy` trong các trường hợp sau:
	* Bạn có một đoạn mã dễ thay đổi, và bạn tách chúng ra khỏi chương trình để dễ bảo trì
	* Bạn muốn tránh sự rắc rối khi phải thực hiện một chức năng nào đó qua nhiều lớp con
	* Bạn muốn thay đổi thuật toán khi sử dụng chương trình

	Ví dụ: Việc sử dụng thuật toán sắp xếp: khi có rất nhiều dữ liệu thì sử dụng QuickSort, lúc khác chỉ có vài ba phần tử thì dùng sắp xếp nổi bọt đã ok rồi
	
### 5 nguyên lý lập trình (Solid principles)

1. **Single Reponsibility Principle**

	Một class chỉ nên giữ một trách nhiệm duy nhất (chỉ có thể sửa đổi class với một lí do duy nhất)
	
	Ví dụ, có một class như sau:
	
	```java
	public class ReportManager {
		public void readDataFromDb();
		public void ProcessData();
		public void PrintReport();
	}
	```
1. **Open/Closed principle**

	Có thể thoải mái mở rộng một class, nhưng không được sửa đổi bên trong class đó. Nghĩa là khi muốn thêm một chức năng cho chương trình, chúng ta nên viết một class mới kế thừa từ clas cũ, chứ không nên sửa class cũ.
	
1. **Liskov Substitution Principle**

	Khi một lớp con kế thừa từ một lớp khác, nó sẽ không làm thay đổi hành vi của lớp đó.
	
	Ví dụ: Lớp Square không được phép thay đổi hành vi của lớp Rectangle (With và Height)
	
1. **Interface Segregation Principle**

	Không nên cài đặt một interface nếu nó không được sử dụng đến. Điều này hay xảy ra khi một interface chứa nhiều hơn một chức năng, và chương trình chỉ cần một chức năng trong interface đó.
	Ví dụ:
	
	```Java
	public interface Animal {
		void fly();
		void run();
		void bark();
	}
	
	public class Bird implements Animal {
		public void bark() {
			// Do nothing
		}
		
		public void run() {
			// Write code about running of the bird
		}
		
		public void fly() {
			// Write code about flying of the bird
		}
	}
	```
	
1. **Dependency Inversion Principle**

	Các module cấp cao không nên phụ thuộc vào các modules cấp thấp, cả 2 nên phụ thuộc vào abstraction
	
	![alt Androdi life cyrcle] (http://laptrinh.vn/attachment.php?attachmentid=46&d=1415081902&thumb=1)
	