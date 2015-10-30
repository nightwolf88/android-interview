##Design pattern

**What is design pattern?**

Design pattern là một tập các mẫu thiết kế, cung cấp ở mức tổng quát các giải pháp để giải quyết các vấn đề chung, hay gặp khi lập trình.

Design pattern giúp giảm thời gian phát triển phần mềm do không mất thời gian để giải quyết các vấn đề chung, đã có lời giải.

Design pattern giúp tổ chức code linh hoạt, code dễ đọc, dễ cập nhật, nâng cấp.

Để làm được design pattern, cần phải nắm được 4 khái niệm của lập trình hướng đối tượng, khái niệm `abstract class` & `interface`.

**Một số pattern phổ biến**

1. **Singleton**

	Một class chỉ có duy nhất một thể hiện tại một thời điểm khi chạy chương trình, nghĩa là đối tượng chỉ được tạo một lần, các lần còn lại chỉ việc sự dụng lại.
	
	Sử dụng `Singleton` khi đối tượng cần sử dụng nhiều nhưng không cần thiết phải tạo lại.
	
	Ví dụ: đối tượng connection database

2. **Observer**

	Là mối quan hệ `một - nhiều` giữa các đối tượng, khi một đối tượng thay đổi trạng thái, thì tất cả các đối tượng còn lại sẽ tự động cập nhật trạng thái theo.
	
	Ví dụ: việc thay đổi ngôn ngữ trong app

3. **Decorator**

	Là khả năng bổ sung trách nhiệm cho đối tượng khi chạy chương trình.
	
	Ví dụ: Một đối tượng `computer` là base của một chiếc máy tính, ta có thể bổ sung thêm ổ đĩa mềm, đĩa cứng, ổ CD vào đối tượng máy tính.
	
	Pattern sẽ đảm bảo nguyên lý `open/close` - nguyên lí chỉ cho phép bổ sung thêm chức năng của đối tượng chứ không được chỉnh sửa.

4. **Factory**

	Factory là pattern cho phép tạo đối tượng, nhưng cách thức tạo đối tượng như thế nào thì lớp con mới là lớp quyết định.
	
	Ví dụ: class `OpenConnectionDatabase` có các lớp con `SqlConnection`, `OracleConnection` thì việc tạo kết nối như thế nào thì mỗi lớp con một kiểu.

5. **Strategy**

	Là pattern cung cấp một tập hợp các thuật toán, và sẽ lựa chọn thuật toán thích hợp để thực hiện khi chạy chương trình.
	
	Ví dụ: cần sắp xếp một danh sách, khi danh sách có nhiều phần tử thì cần phải lựa chọn `quicksort`, nhưng khi danh sách có một vài phần tử, ta chỉ cần lựa chọn thuật toán `nổi bọt`
	
##Java core

**Java collection**

|Name|Description|Item|
|---|---|---|
List|Collection allow duplicate item|ArrayList, LinkedList|
Set|Collection cannot duplicate item|HashSet, TreeSet|
Map|Key/value collection|HashMap, TreeMap, HashTable|

**Difference of ArrayList & LinkedList**