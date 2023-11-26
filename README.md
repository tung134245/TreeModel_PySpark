# TreeModel_PySpark
TÌM HIỂU MÁY PHÁT HIỆN XÂM NHẬP

Phần mềm phát hiện sự xâm nhập mạng sẽ bảo vệ mạng máy tính khỏi những người dùng trái phép, kể cả những người trong nội bộ. Nhiệm vụ học tập của bộ phát hiện xâm nhập là xây dựng một mô hình dự đoán (tức là một bộ phân loại) có khả năng phân biệt giữa các kết nối “xấu”, được gọi là xâm nhập hoặc tấn công, và các kết nối thông thường “tốt”.

Chương trình đánh giá phát hiện xâm nhập DARPA năm 1998 do MIT Lincoln Labs chuẩn bị và quản lý. Mục tiêu là khảo sát và đánh giá nghiên cứu về phát hiện xâm nhập. Một bộ dữ liệu tiêu chuẩn cần được kiểm tra, bao gồm nhiều loại xâm nhập được mô phỏng trong môi trường mạng quân sự, đã được cung cấp. Cuộc thi phát hiện xâm nhập KDD năm 1999 sử dụng phiên bản của bộ dữ liệu này.

Lincoln Labs đã thiết lập một môi trường để thu thập dữ liệu kết xuất TCP thô trong chín tuần cho mạng cục bộ (LAN) mô phỏng mạng LAN điển hình của Không quân Hoa Kỳ. Họ vận hành mạng LAN như thể đó là một môi trường thực sự của Lực lượng Không quân, nhưng lại tấn công nó bằng nhiều cuộc tấn công.

Dữ liệu huấn luyện thô là khoảng 4 gigabyte dữ liệu kết xuất TCP nhị phân được nén từ lưu lượng truy cập mạng trong bảy tuần. Điều này đã được xử lý thành khoảng năm triệu bản ghi kết nối. Tương tự, dữ liệu thử nghiệm trong hai tuần mang lại khoảng hai triệu bản ghi kết nối.

Kết nối là một chuỗi các gói TCP bắt đầu và kết thúc tại một số thời điểm được xác định rõ ràng, giữa đó dữ liệu truyền đến và đi từ địa chỉ IP nguồn đến địa chỉ IP đích theo một số giao thức được xác định rõ ràng. Mỗi kết nối được gắn nhãn là bình thường hoặc là một cuộc tấn công, với chính xác một loại tấn công cụ thể. Mỗi bản ghi kết nối bao gồm khoảng 100 byte.

Các cuộc tấn công rơi vào bốn loại chính:

- DOS: từ chối dịch vụ, ví dụ như lũ đồng bộ;
- R2L: truy cập trái phép từ máy từ xa, ví dụ đoán mật khẩu;
- U2R: truy cập trái phép vào các đặc quyền của siêu người dùng (root) cục bộ, ví dụ: các cuộc tấn công ``tràn bộ đệm'' khác nhau;
- Probe: giám sát và thăm dò khác, ví dụ, quét cổng.
