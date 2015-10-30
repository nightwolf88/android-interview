1. **Activity**

	Một màn hình đang hiện lên cho người dùng thao tác là một activity.
	
	*Activity cycle:*
	
	![alt Androdi life cycle] (http://developer.android.com/images/activity_lifecycle.png)
	
	* `onCreate()`: được gọi khi activity khởi tạo lần đầu. Là nơi khởi tạo view, data, bind data to list. `onCreate()` cung cấp `Bundle` bao gồm trạng thái của `activity` trước.
	* `onStart()`: được gọi khi `activity` hiện lên cho người dùng.
	* `onRestart()`:
	* `onResume()`: Được gọi khi activity bắt đầu tương tác với người dùng, lúc này `activity` ở trên top của stack.
	* `onPause()`: 
	* `onStop()`: Gọi khi `activity` không hiện lên cho người dùng sau một khoảng thời gian. 
	* `onDestroy()`:
	
2. **Services**

	`Service` là thành phần chạy dưới nền của ứng dụng để thực hiện một thao tác lâu dài, `service` là thành phần không có giao diện người dùng.
	
	*Có 2 loại service:*
	* `Started service`: Là service được bắt đầu giống như các component khác, bắt đầu bằng cách gọi hàm `startService()`. Thông thường, 1 `start service` thực hiện một hành động đơn lẻ và không trả về kết quả cho đối tượng gọi nó. Ví dụ, thao tác upload file, hoặc download file thông qua mạng, khi thực thi xong thì nó tự động dừng lại
	* `Bound service`: là kiểu service ràng buộc, được gọi qua hàm `bindService()`, là kiểu service cung cấp một interface để đối tượng gọi có thể tương tác được với service đó. Ví dụ như service play music, có thể pause, stop service play music.

3. **Content Provider**

	Là thành phần cung cấp dữ liệu từ một ứng dụng đến một ứng dụng khác dựa trên các `Request`

4. **Broadcast Receiver**

	Là bộ thu nhận các bản tin cho apps (bản tin có thể phát đi từ trong app, hoặc thu nhập từ bên ngoài)

5. **Fragment**

	`Fragment` là một đối tượng được nhúng vào `Activity`, được xem như là một thành phần của activity (sub-activity).
	
	Một fragment cũng có vòng đời riêng của nó, và nó phụ thuộc chặt chẽ vào vòng đời của activity.
	
	*Fragment cycle:*
	
	![alt Androdi life cycle] (http://developer.android.com/images/fragment_lifecycle.png)
	
	* **Init fragment:**
		* *onAttach()*
		* *onCreate()*
		* *onCreateView()*
		* *onActivityCreated()*
	* **Fragment visible:**
		* *onStart()*
		* *onResume()*
	* **Fragment foreground:**
		* *onPause()*
		* *onStop()*
	* **Fragment destroy:**
		* *onPause()*
		* *onStop()*
		* *onDestroyView()*
		* *onDestroy()*
		* *onDetach()*

6. **Layout**
7. **Cache**
8. **Bitmap & image processing**
9. **SQLite**
10. **Asynctask, Thread, Handler**
11. **Context**