### Android architecture

* ***Applications:*** là tầng trên cùng, chứa các ứng dụng mà developer phát triển
* ***Application frameworks:*** là tầng chứa các API cho Android Java, cung cấp cho tầng applications.
* ***Libraries & Android Runtime:*** là các driver, thư viện làm việc trực tiếp với các thiết bị phần cứng
* ***Linux kernel:*** là nhân của hệ thống, cung cấp các chức năng cơ bản như quản lí tiến trình, bộ nhớ, máy ảnh, bàn phìm...

### Android life cyrcle

![alt Androdi life cyrcle] (http://developer.android.com/intl/ja/images/activity_lifecycle.png)

### Android component

1. ***Activity*** 

	Là những thành phần tương tác với người dùng (người dùng thấy được, tương tác được với ứng dụng)

1. ***Services*** 

	Những hoạt động chạy ngầm trong ứng dụng được gọi là services, services để thực hiện các hoạt động lâu dài hoặc thực hiện công việc cho các xử lý từ xa.

1. ***Broadcast Receivers*** 
	Là thành phần để nhận thông điệp từ ứng dụng khác hoặc từ hệ thống (thu nhập các intent từ bên ngoài gửi tới)

1. ***Content providers*** 

	Quản lý một tập hợp các dữ liệu được chia sẻ của ứng dụng. Thông qua content provider, các chương trình khác có thể truy xuất hoặc thậm chí thay đổi các dữ liệu của một ứng dụng
	
1. ***Intent***

	Được sử dụng để truyền các thông báo nhằm khởi tạo một Activity hoặc service để thực hiện công việc bạn muốn
	
1. ***Notification***

	Đưa ra các cảnh báo mà không làm ảnh hưởng đến các activity đang hoạt động
	
1. ***Manifest***

	Mô tả các thông tin cần thiết của ứng dụng cho hệ điều hành Android.

### View/UI/Layout

![alt Androdi life cyrcle] (http://www.vogella.com/tutorials/AndroidCustomViews/images/xandroid_viewhierarchy10.png.pagespeed.ic.nQTkkQQ3Y8.png)

View là tất cả các thành phần nhìn thấy được trên màn hình.

1. ***How to a view draw on screen***

	* Measuring pass: - tính toán kích thước của view
	* Layout pass: tính toán vị trí của view
	* Draw: Vẽ view sau khi đã tính toán vị trí và kích thước.

1. ***Type of layout***

	* *LinearLayout:* Sắp xếp các view con lần lượt theo chiều ngang hoặc chiều dọc
	* *RelativeLayout:* Sắp xếp view dựa vào quan hệ các view với nhau
	* *FrameLayout:* Chỉ đơn giản là một vùng hiển thị một item con bên trong, item con sẽ được đặt tại góc trái bên trên của frame.

1. ***RelativeLayout và LinearLayout***

	Chi phí tính toán của RelativeLayout lớn hơn nhiều so với LinearLayout. LinearLayout chỉ đơn giản là sắp sếp theo thứ tự, hết cái này đến cái kia, còn RelativeLayout là tính view A phụ thuộc vào view B, do đó phải tính xong vị trí, kích thước view A mới tính đến cái B, do đó, chi phí tính toán sẽ tăng theo cấp số nhân.
	
1. ***ScrollView***
	
1. ***ListView***

### Android networking

1. ***Networking***

	Tất cả các yêu cầu kết nối mạng trong app được gọi là networking. Android sử dụng giao thức http để kết nối mạng, để thực hiện một request http, ta cần các bước sau:
	* Tạo đối tượng chưa giao thức request (get, post) `HttpGet` với tham số là url
	* Tạo `HttpClient` để thực thi giao thức
	* Tạo đối tượng `HttpResponse` để nhận kết quả trả về khi thực thi HttpClient

1. ***Web services***

	Là các dịch vụ trên server mà client có thể gọi bằng giao thức http
	
1. ***JSON***

	JSON là một chuẩn (định dạng) để gửi dữ liệu giữa client và server với nhau.

1. ***Soap, Rest web services***

* *Soap:* (Simple Object Access Protocol) là giao thức truy vấn dữ liệu, nó chỉ đơn giản là request lên server và lấy về xml của object

* *Rest:* là cách thức web services trao đổi dữ liệu độc lập platform với client (android, iOS, Window phone). Rest có thể hỗ trợ thêm các truy vấn như thêm, sửa, xóa khi client request webservices.


### Caching

Cache là cơ chế lưu những dữ liệu được sử dụng thường xuyên và ít bị thay đổi vào bộ nhớ để đảm bảo cho việc truy xuất nhanh hơn trong các lần tái sử dụng lần sau. Ví dụ: cache ảnh, audio từ internet.