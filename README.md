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
 - Trò chơi bắn bong bóng: - Trò chơi bắn bong bóng rất phổ biến cũng sử dụng đệ quy trong đó. Nó thường tìm thấy tất cả các bong bóng cùng màu có thể có ở cả bốn hướng và cả hai đường chéo. Các bong bóng này được kết nối với nhau và phát nổ nếu bong bóng cùng màu được ném vào chúng. Trò chơi này giống như bài toán flood fill của giải thuật đệ quy.

![bg](https://lh6.googleusercontent.com/8Vp4pHjX1a5Ixen3KAcD7r6jC3YMwQaGIyj6Q49iDlKx0sZ0l2sasKdpk7-pauiqErq8wEbI4ryalYSnB0ob4UpXBQ4JcvrNFGUl02NKh64iLE6LmAvlHfj1c_cAo06nTmAnlIyX) 
 - Cấu trúc dữ liệu cây: Cấu trúc dữ liệu cây sẽ không tồn tại nếu không có đệ quy. Chúng ta cũng có thể giải quyết vấn đề đó bằng cách dùng vòng lặp nhưng điều đó sẽ rất khó khăn. Đối với các vấn đề nhỏ hơn, vòng lặp sẽ hoạt động tốt nhưng đối với cây lớn hơn, vòng lặp sẽ trở nên đau đầu khi sử dụng. bởi vì khi kích thước cây tăng lên thì kích thước code cũng sẽ tăng theo. Nhưng với sự trợ giúp của đệ quy, kích thước code sẽ giảm đi đáng kể.
 - Thuật toán sắp xếp: Hầu hết các thuật toán sắp xếp đều sử dụng đệ quy để sắp xếp dữ liệu theo điều kiện cho trước. Nhiều thuật toán sắp xếp như QuickSort, MergeSort, v.v. Sử dụng đệ quy để sắp xếp dữ liệu. Một số thuật toán tìm kiếm giống như BinarySearch sử dụng khái niệm đệ quy.
 - Xử lý ngôn ngữ tự nhiên: Trong xử lý ngôn ngữ tự nhiên, đệ quy được sử dụng để phân tích câu, phân tích cú pháp và sinh từ vựng.
Với sự phát triển của khoa học máy tính và công nghệ thông tin, đệ quy đã được sử dụng rộng rãi trong nhiều lĩnh vực và được xem là một công cụ mạnh mẽ trong việc giải quyết các bài toán phức tạp.

## 4, Các tính chất chủa đệ quy
3 tính chất bắt buộc của giải thuật đệ quy:
 - Một giải thuật đệ quy phải tự gọi chính nó.
 - Một giải thuật đệ quy phải có trường hợp cơ sở. Khi đến trường hợp đó thì giải thuật đệ quy này sẽ dừng lại.
 - Một giải thuật đệ quy phải thay đổi trạng thái của nó và ngày càng tiến gần tới trường hợp cơ sở sau mỗi lần gọi.
Ngoài ra cần lưu ý một số định lý liên quan đến đệ quy như sau:
 - Định lý về đệ quy: Định lý này chỉ ra rằng một thuật toán đệ quy có thể được chuyển đổi thành một thuật toán không đệ quy, và ngược lại.
 - Định lý đệ quy đơn giản: Định lý này chỉ ra rằng một bài toán đệ quy có thể được giải quyết bằng một thuật toán đệ quy đơn giản nếu các bài toán con của nó được giải quyết bằng các bài toán con đơn giản hơn.

## 5, Ý tường thuật toán
Đệ quy có bản chất tương tự như một vòng lặp, khi mà ở mỗi bước đệ quy, ta lại lặp đi lặp lại một công việc nhất định. Để có được ý tưởng khi triển khai giải một bài toán, ta phải nhận ra rằng bài toán có thể được chia thành các bài toán con nhỏ hơn, và các bài toán con này lại có thể được chia thành các bài toán con nhỏ hơn nữa. Quá trình này được lặp đi lặp lại cho đến khi chúng ta có thể giải quyết các bài toán con đơn giản một cách trực tiếp (base case). Việc này đòi hỏi một khả năng tư duy trừu tượng và phân tích, và có thể giúp giải quyết các bài toán phức tạp một cách hiệu quả và dễ dàng hơn.

## 6, Mã giả
Bài toán: Tìm đường đi từ điểm này đến điểm kia trong bản đồ. Coi bản đồ là một cấu trúc dữ liệu cây.

```
struct Node {
  int x;
  int y;
  Node *left; 
  Node *right; 
}
```
a, Phương pháp giải quyết: Thuật toán Depth-first Search (DFS)
 - Design: Chọn một nút bất kì, dánh dấu nút đó và di chuyển sang một nút chưa được dánh dấu liền kề và lặp lại điều trên cho đến khi không còn nút liền kề. Sau đó backtrack lại và tìm các nút chưa được đánh dấu và đi theo chúng. Khi đến đích thì dừng lại và in quãng đường di chuyển ra.

b, Mã giả
```
procedure DFS(node):
    mark node as visited
    process(node)
    if node.x and node.y equal target 
        then breaks;
    for each neighbor in node.neighbors:
        if neighbor is not visited:
            DFS(neighbor)
```
c, Flow chart

![bg](https://techindetail.com/wp-content/uploads/2021/09/flowchat-depth-first-traversal-648x720.png.webp) `#fcfafa`

## 7, Cài đặt
Bước 1: Tạo một mảng để theo dõi các nút đã truy cập.
Bước 2: Chọn một nút bắt đầu.
Bước 3: Tạo một ngăn xếp trống và đẩy nút bắt đầu vào ngăn xếp.
Bước 4: Đánh dấu nút bắt đầu là đã truy cập.
Bước 5: Trong khi ngăn xếp không trống, hãy làm như sau:
 - Bật một nút từ ngăn xếp.
 - Xử lý hoặc thực hiện bất kỳ thao tác cần thiết nào trên nút đã bật.
 - Nhận tất cả các hàng xóm liền kề của nút bật lên.
 - Đối với mỗi hàng xóm liền kề, nếu nó chưa được thăm, hãy làm như sau:
 - Đánh dấu hàng xóm là đã đến thăm.
 - Đẩy hàng xóm vào ngăn xếp.
Bước 6: Lặp lại bước 5 cho đến khi hết ngăn xếp hoặc đến đích.

## 8, Đánh giá
 - Bất biến của thuật toán: dùng tọa độ của nút hiện tại so sánh với nút đích đến để dừng vòng lặp.
 - Time Complexity: Thuật toán này có độ phức tạp thời gian là O(V + E) trong đó V là số đỉnh và E là số cạnh. Điều này là do thuật toán khám phá từng đỉnh và cạnh chính xác một lần.
 - Space Complexity: Độ phức tạp không gian của DFS là O(V). Điều này là do trong trường hợp xấu nhất, ngăn xếp sẽ chứa tất cả các đỉnh của bản đồ.

## 9, Cải tiến: Breadth First Search(BFS)
 - a, Ý tưởng: Thuật toán tìm kiếm theo chiều rộng (BFS) được sử dụng để tìm kiếm cấu trúc dữ liệu dạng cây hoặc biểu đồ cho một nút đáp ứng một bộ tiêu chí. Nó bắt đầu từ gốc hoặc biểu đồ của cây và tìm kiếm tất cả các nút ở mức độ sâu hiện tại trước khi chuyển sang các nút ở mức độ sâu tiếp theo. 
 - b, Design: 
 Bước 1: Chọn một đỉnh khời đầu,
 Bước 2: đánh dấu đỉnh đó và kiểm tra các đỉnh xung quanh. 
 Bbước 3: lặp lại bước 2 với các đỉnh được đánh dấu cho đến khi đến đích
 - c, mã giả:
 ```
 Breadth_First_Search( Graph, X ):
    Let Q be the queue
    Q.enqueue( X )     // Inserting source node X into the queue
    Mark X node as visited.

    While ( Q is not empty )
        Y = Q.dequeue( )     // Removing the front node from the queue

    Process all the neighbors of Y, For all the neighbors Z of Y
    If Z is not visited:
        Q. enqueue( Z )     // Stores Z in Q
        Mark Z as visited
 ```
 - d, flow chart:
 - 
 ![#FFFFFF](https://techindetail.com/wp-content/uploads/2021/09/flowchart-breadth-first-traversal-471x720.png.webp)
 
 - e, cài đặt
    - Bước 1: chọn bản đồ và địa điểm cần đến.
    - Bước 2: chọn điểm bắt đầu (gọi là v1)
    - Bước 3: Sử dụng hai cấu trúc dữ liệu sau để duyệt bản đồ. Mảng đã truy cập (kích thước của biểu đồ) và cấu trúc dữ liệu hàng đợi
    - Bước 4: Thêm đỉnh bắt đầu vào mảng đã truy cập, sau đó, bạn thêm các đỉnh liền kề của v1 vào cấu trúc dữ liệu hàng đợi.
    - Bước 5: Bây giờ, sử dụng khái niệm FIFO, loại bỏ phần tử đầu tiên khỏi hàng đợi, đặt nó vào mảng đã truy cập, sau đó thêm các đỉnh liền kề của phần tử đã loại bỏ vào hàng đợi.
    - Bước 6: Lặp lại bước 5 cho đến khi đến đích.

- f, đánh giá
 - Bất biến của thuật toán: dùng tọa độ của nút hiện tại so sánh với nút đích đến để dừng vòng lặp.
 - Time Complexity: Thuật toán này có độ phức tạp thời gian là O(V + E) trong đó V là số đỉnh và E là số cạnh. Điều này là do thuật toán khám phá từng đỉnh và cạnh chính xác một lần.
 - Space Complexity: Độ phức tạp không gian của DFS là O(V). Điều này là do trong trường hợp xấu nhất, ngăn xếp sẽ chứa tất cả các đỉnh của bản đồ.
 - Tuy độ phức tạp là như nhau nhưng đoạn đường do thuật toán này đưa ra sẽ ngắn hơn nhiều so với DFS.

## 10, Bài tập
Sau đây là một vài ví dụ về bài tập đệ quy:
- Tính giai thừa: Giai thừa của một số n là tích của dãy số dương từ 1 đến n, hay có thể gọi là tích của n với giai thừa của (n-1). Do đó ta có thể thiết kế hàm đệ quy cho (n-1) cho đến khi n bằng 1.
- Tìm số Fibonacci: Số fibonacci thứ n là tổng của số fibonacci thứ (n - 1) và số fibonacci thứ (n - 2) với f(0) = 0 và f(1) = 1. Để tính số fibonacci thứ n ta có thể gọi đệ quy cho (n - 1) và (n - 2) cho đến khi n = 0 hoặc n = 1 thì trả về chính nó.
- Sắp xếp mảng: Chọn một phần tử bất kỳ trong mảng làm chốt, rồi phân tách mảng thành hai phần: một phần chứa các phần tử nhỏ hơn hoặc bằng chốt và một phần chứa các phần tử lớn hơn chốt. Ta sử dụng đệ quy để sắp xếp hai phần này và ghép lại với nhau.
- Duyệt và tìm kiếm trong cây nhị phân: Đệ quy thường được ứng dụng trong các cấu trúc dữ liệu như cây nhị phân, danh sách liên kết, ... Ta có thể giải đa số các bài tập liên quan đến các cấu trúc dữ liệu trên bằng đệ quy.

> research source: 
> - geeksforgeeks.org.




 
