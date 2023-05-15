# Self-study-Recursion

## 1, Khái niện về đệ quy
Bản chất của giải thuật đệ quy là phân tách một bài toán lớn thành những bài toán nhỏ hơn và dễ giải hơn, sau đó tìm cách kết hợp lời giải của các bài toán nhỏ lại thành lời giải cho bài toán lớn ban đầu. Sử dụng giải thuật đệ quy, một số bài toán có thể được giải quyết khá đơn giản.

## 2, Ví dụ 
Đệ quy có thể được sử dụng để giải quyết đa dạng các bài toán như:

 - Tính giai thừa của một số nguyên dương n.
 - Tìm kiếm tuyến tính trong một mảng.
 - Tìm kiếm nhị phân trong một mảng đã được sắp xếp.
 - Duyệt cây nhị phân và in ra các node.
 - Sắp xếp một mảng bằng phương pháp quicksort.

## 3, Ứng dụng
 - Trò chơi bắn bong bóng: - Trò chơi bắn bong bóng rất phổ biến cũng sử dụng đệ quy trong đó. Nó thường tìm thấy tất cả các bong bóng cùng màu có thể có ở cả bốn hướng và cả hai đường chéo. Các bong bóng này được kết nối với nhau và phát nổ nếu bong bóng cùng màu được ném vào chúng. Trò chơi này giống như bài toán lấp flood fill của giải thuật đệ quy.
(https://lh6.googleusercontent.com/8Vp4pHjX1a5Ixen3KAcD7r6jC3YMwQaGIyj6Q49iDlKx0sZ0l2sasKdpk7-pauiqErq8wEbI4ryalYSnB0ob4UpXBQ4JcvrNFGUl02NKh64iLE6LmAvlHfj1c_cAo06nTmAnlIyX)
 - Cấu trúc dữ liệu cây: Cấu trúc dữ liệu cây sẽ không tồn tại nếu không có đệ quy. Chúng ta cũng có thể giải quyết vấn đề đó bằng cách dùng vòng lặp nhưng điều đó sẽ rất khó khăn. Đối với các vấn đề nhỏ hơn, vòng lặp sẽ hoạt động tốt nhưng đối với cây lớn hơn, vòng lặp sẽ trở nên đau đầu khi sử dụng. bởi vì khi kích thước cây tăng lên thì kích thước code cũng sẽ tăng theo. Nhưng với sự trợ giúp của đệ quy, kích thước code sẽ giảm đi đáng kể.
 - Thuật toán sắp xếp: Hầu hết các thuật toán sắp xếp đều sử dụng đệ quy để sắp xếp dữ liệu theo điều kiện cho trước. Nhiều thuật toán sắp xếp như QuickSort, MergeSOrt, v.v. Sử dụng đệ quy để sắp xếp dữ liệu. Một số thuật toán tìm kiếm giống như BinarySearch sử dụng khái niệm đệ quy.
 - Xử lý ngôn ngữ tự nhiên: Trong xử lý ngôn ngữ tự nhiên, đệ quy được sử dụng để phân tích câu, phân tích cú pháp và sinh từ vựng.
Với sự phát triển của khoa học máy tính và công nghệ thông tin, đệ quy đã được sử dụng rộng rãi trong nhiều lĩnh vực và được xem là một công cụ mạnh mẽ trong việc giải quyết các bài toán phức tạp.

## 4, Các tính chất chủa đệ quy
