
1. Build project trên Web Mobile, Web Desktop, Android trong thư mục ./Cocos_HelloWord/build
    - Web Mobile : Done.
    - Web Desktop : Done.
    - Android : 
    - Deploy web desktop : https://nhontd93.github.io/Deploy_Cocos_BuildWebDesktop/
2. Cài đặt Module Lodash trong thư mục ./Cocos_HelloWorld/packages : Done.
    Bước 1: Mở terminal của folder package
	Bước 2: nhập dòng lệnh: npm i —save lodash
3. Các Tham số trên Screen game:
	- Frame time (ms): thời gian để tạo mỗi frame. Thời gian tối đa để tạo ra 1 frame là 16ms, tuy nhiên trình duyệt cần ít nhất 6ms để hiển thị frame. Do đó ta chỉ còn tối đa 10ms để tạo 1 frame cho animation.
	- Framerate(FPS: Frames Per Second): là số lượng frame được truyền trong 1s, càng nhiều frame được truyền trong 1s thì hành động đó càng mượt.
	- Drawcall: là 1 command buffer giữa CPU và GPU. Khi CPU cần gọi giao diện đồ họa thì nó sẽ thêm lệnh vào command buffer. Khi GPU hoàn thành lệnh render cuối cùng thì nó sẽ tiếp tục thực hiện lệnh tiếp theo từ command buffer. Có nhiều lệnh trong command 	buffer, và Drawcall là 1 trong số đó. CPU cần xử lý rất nhiều thứ khi gửi một drawcall. Nó bao gồm một số thứ như data, status, command… Một số lỗi hiển thị là do tốc độ render của GPU nhanh hơn tốc độ gửi của drawcall. Có thể lần hiển thị cuối cùng đã kết thúc mà CPU vẫn đang tính toán drawcall. Performance bottleneck của drawcall nằm ở CPU. Cách hiệu quả nhất để tối ưu hóa render hàng loạt drawcall là hợp nhất một số lượng lớn các drawcall nhỏ thành một drawcall lớn để giảm số lượng drawcall.
	- Game Logic: là một lệnh của CPU gửi tới GPU để thay đổi các thuộc tính, trạng thái của đối tượng trong project.
	- Renderer: là thời gian để tạo ra một hình ảnh hai hoặc ba chiều.
	- WebGL(Web Graphics Library) : là một API JavaScript để render hình ảnh 2D và 3D trong bất kỳ trình duyệt web tương thích nào mà không cần sử dụng các plug-in.