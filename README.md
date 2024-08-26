# Junior_Interview
## Câu 1: TypeScript có ưu nhược điểm gì. Em có biết trường hợp cụ thể nào gây ra nặng cho dự án?
- TypeScript: là mã nguồn mở của js. Chủ yếu dùng và xây dựng dự án ứng dụng phức tạp.

## Câu 2: Nextjs là gì,em hiểu biết những gì về next
- Nextjs là mã nguồn mở dựa trên nền tảng của React, cho phép xây dựng các trang web tĩnh có tốc độ nhanh
- Tự động tạo route. Chỉ cần tạo file .tsx trong pages => tự tạo đường dẫn route là /abl=out
- SSR(Server-side rendering): 
  - Cơ chế như sau: 
    - Khu user truy cập trang web, => gửi tới server
    - Server nhận => ren ra html
    - Trả html kèm ss js 
    - render ra ui
    - browser tải xuống js và thực thi các câu lệnh js
    - web load xong có thể tương tác bthg
  - Nhược điểm: Server xử lý nhiều => quá tải
    - Khi user chuyển trang thì cả trang load lại dữ liệu từ server

-CSR(Client side rendering):

## Câu 3: Ưu và nhược điểm của React
## Câu 4: VirtualDOm 

## Câu 5: Các thành phần chính của redux

## Câu 6: useRef có tác dụng gì,sử dụng như nào, có làm thay đổi rerender lại không
- useRef cho phéo tạo ra tham chiếu có thể thayd đổi đến một giá trị hoặc một phần tử dom.
- 



# React Native
## Câu 1: Nếu có 10k item e xử lý ntn
- Em sẽ dùng FlatList để render nó ra 
- Có thuộc tính removeClippedSUbView: Tức là nó sẽ loại bỏ các chế độ xem bên ngoài khung nhìn khỏi quá trình hiển thị khung nhìn chính.
- maxToRenderPerBatch: Hiển thị số khung nhìn 

## Câu 2: Có máy thread chạy trong react native
Main thread, js thread

## Câu 3: useCallback và useMemo

# Phỏng vấn 
## Câu1
- useMemo => trả 1 giá trị 
- useCallback => trả 1 hàm

**Cách trả lời như sau:** 
- useMemo và useCallback là hai hook React giúp tối ưu hiệu suốt trong function component. Chức năng là ghi nhớ các giá trị và hàm để tránh bị rerender khi không cần thiết.
- Đối với useMemo:
  - Ghi nhớ giá trị: Trả về giá trị của biểu thức phụ thuộc vào dependence
  - Tái sử dụng: Thay vì tính toán lại mà nó trả về giá trị hàm luôn
- Dối với useCallback:
  - Ghi nhớ hàm: 
  - Giữ nguyên tham chiếu: Khi các tham số phụ thuộc không đổi thì useCallback sẽ trả về một tham chiếu hàm được ghi nhớ thay vì tạo ra hàm mới
  => Tuy nhiên useCallback và usememo nên dùng cho đúng chứ không nên lạm dụng nó. Nếu lạm dụng thì có thể sẽ gây ra hiện tượng chậm trong lần render đầu tiên.
## Câu 2: 
Redux saga hoạt động?
Redux, zustand có cơ chế presit không ( là cái lưu lại khi out khỏi app )
- Trả lời
- Redux: Redux là một thư viện quản lý trạng thái global sate. Nó có các thành phần chính như sau
  - Action: Là nơi muốn thay đổi với trạng thái
  - Reducers: Là các 
  - Store: Nơi lưu trữ tạng thái 
- Redux toolkit: 
  - Cung cấp hàm configureStore, createReducer, createSlide, tạo dễ dang hơn
  - Về redux saga thì e có đọc trong dự án thấy mấy a chủ yếu dùng để tích hợp gọi api.
- Cơ chế redux presist là haotj động bằng cách lưu trữ redux vào cục bộ như async storage.
## Câu3: Sử dụng thông báo với firebase
- Sử dụng với thư viện react native firebase
- Cài **yarn add @react native firrebase/app và firebase/mess**
- Vào -> android -> app0> src -> build.gradie -> Chọn namespace
- Cần có FCM Token rồi vào fcm token test gửi thông báo
- Có FCM Token và backend sẽ config để gửi thông báo về cho minh.
- Ví dụ màn hình chat: Sẽ nhúng deeplink và qua các stack cha mà mình đã cấu hình => màn chat. 
Cấu hình firebase
## Câu4: lifecycle hoạt động ra sao
- Các giai đoạn của lifecycle như sau:
  - Initialization: Khởi tạo
  - Mounting: Gắn phần tử vào dom
  - Updateting: Cập nhật props, states thay đổi
  - Unmont: Gỡ khỏi Dom
  - return trong useEffect nằm trong unmount
## Câu5: 
- Nếu ko dùng react query thì có thể dùng gì gọi api(useEff)
- Xử lý bất đồng bộ ntn
  - Trả lời: Em thường sử dụng async/await để có thể xử lý bất đồng bộ trong code
## Câu 6: Từng đẩy app lên ch-play chưa
- Quy trình đẩy như sau: 
  - Cần có tài khoản development
  - Tạo app, thêm ảnh, thông tin, logo, chính sách
  - Tạo bản phát hành
  - Đẩy file .âb lên (Khu tạo nên để key cùng thư mục)
  - đợi duyệt
## Câu 7: Dùng gì để điều hướng các màn hình, truyền dữ liệu trong react navigation như thế nào
Đầu tiên e sử dụng thư viện điều hướng là react navigation, nó là thư viện khá nổi tiếng trong react native. Khi em muốn truyền dữ liệu của nó qua màn hình khác, thì e sẽ truyền vào trong và khi lấy ra sẽ dùng route.params

## Câu 8: useRef dùng như nào
- Trả lời
  - useRef là một hook của react nó cho phép truy cập vào 1 phần tử trong component, và có thể tương tác trực tiếp với phần tử đó.
  - Các bước: 
    - Tạo ref
    - Sau đó gán ref vào useRef thường khởi tạo là null
    -  Sau đó truy cập vào phần tử và dùng thuộc tính .current đẻ lấy giá trị của nó
    -  Nó sẽ không render lại component
## Câu 9: Câu hỏi về authen token. Khi token hết hạn e refetch token thì chủ yếu làm gì
- Token là xác thực quá trình xác minh danh tính của người dùng, ngăn chặn các truy cập trái phép vào dữ liệu. 
- Có 3 loại token: Asscesstoken refetch token và authorize token
- Refetch token là quá trình lấy token mới khi token hiện tại bị hết hạn. 
- Cách dùng: 
  - Người dùng sẽ gửi refetch token đến server để có thể lấy được token mới. 
- Lợi ích: Cải thiện trải nghiệm của người dùng, không cần đăng nhập lại thường xuyên
- ASS token thường lưu trữ ở local storage hoặc là key chain
- Lợi ích: 
  - cải thiện hiệu suất
  - cải tiện trải nghiệm người dùng
  - tăng cường bảo mật
  - tăng tính linh hoạt

## Câu 10: Liên quan về git
- Là hệ thống quản lý phiên bản, được sử dụng để thay đổi các tệp và thư mục.

## Câu 11: Xử lý bất đồng bộ có bao nhiêu cách. Nêu rõ từng cách


## Câu 12: Xử lý firebase gửi thông báo về. Nếu thông báo gửi về, người dùng thoát app ra và token bị hết hạn refetch token ko lấy được token mới thì khi click vào thông báo có vao trực tiếp đó ko


## Câu 13: Js là một ngôn ngữ đơn luồng, tại sao Js có thể chạy mà tưởng như đang chạy xử lý cùng một lúc
Js là ngôn ngữ đơn luồng nhưng nó lại chạy tạo cảm giác xử lý nhiều luồng cùng một lúc nhờ vào kỹ thuật bất đồng bộ.
Trong js có 3 loại bất đồng bộ: 
**Cách1**: Callback
- là hàm được truyền vào một hàm khác để thực thi sau khi hàm đó được hoàn thành. 
- Nhược điểm: Dễ sinh ra callback hell tức là các callback bị lồng nhau
```js
function getData(url, callback) {
  // Gửi yêu cầu đến máy chủ
  fetch(url)
    .then(response => response.json())
    .then(data => callback(data))
    .catch(error => console.error(error));
}

getData('https://jsonplaceholder.typicode.com/todos/1', function(data) {
  console.log(data);
});
```

**Cách2** Async await: Để giải quyết tình trạng callback hell
- Là cú pháp dùng để xử lý bất đồng bộ một cách dễ dàng hơn. Nó giúp việc đọc code dễ hơn.
  - Nó thực hiện tuần tự.

**Cách3** Promise là cách quản lý và xử lý bất đồng bộ dễ hơn so với useCallback
- Lý do: 
  - Sử dụng try catch để xử lý lỗi
  - Trạng thái: 
    - pending: Được tạo
    - fulfilled: hoàn thành
    - rejected: bị từ chối
  - Hai phương thức chính: 
    - resolve: trả về kết quả của tác vụ bất đồng bộ
    - reject: 
Ví dụ: 
```js
function fetchData(url) {
  return new Promise((resolve, reject) => {
    fetch(url)
      .then(response => response.json())
      .then(data => resolve(data))
      .catch(error => reject(error));
  });
}

fetchData('https://jsonplaceholder.typicode.com/todos/1')
  .then(data => console.log(data))
  .catch(error => console.error(error));
```
  - promise.all: Chờ đợi tất cả promisse trong mnagr hoàn thành. Tức là tất cả tác vụ được thực hiện cùng một lúc.

## Câu14: Sự khác nhau giữa next và vite là gì 
- Vite: Sử dụng kiến trúc client-side rendering kế.
- Next: Sử dụng server side rendering

## Câu 15: So sánh ssr và csr
- SSR: mã html được tạo ra trên server rồi gửi tới trình duyệt người dùng
  - SEO tốt hơn
  - Hiệu suất tải trang lần đầu nhanh hơn
  - Tăng khả năng truy cập
  - Được tích hợp sẵn route
- Nhược điểm:
  - Tải trọng server cao hơn. 
  - Chuyển trang tệ hơn vì cần ở server gửi về
  - Có thể gây ra chậm nếu nhiều request
CSR: Là html được gửi tới trình duyêt
  - Tốc độ tải trang ở các lần kế tiếp nhanh hơn
  - Trải nghiệm người dùng mượt hơn
- Nhược điểm:
  - SEO kém hơn
  - tốc độ tải trang lần đầu chậm hơn
  
# Hiểu rõ redux. Now cày thôi nào
## Context:
  Môi lần context thay đổi thì những thằng con nào sử dụng chúng đều bị thay đổi theo (rerender dù dùng memo hay bất cứ gì)


# Luyện tập các hàm js
## Các hàm xử lý với mảng trong js
### 1. Hàm at
``` js
let array = ['a', 'b', 'c']
console.log(array.at(2)) // kết quả là 'c'
```

### 2. Hàm concat()
```js
let array1 = [1, 2];
let array2 = [3, 4];
console.log(array1.concat(array2)) // => kết quả là [1,2,3,4]
```
Nó không thay đổi mảng cũ
### 3. Hàm every()
Trả về giá trị true hoặc false. Nếu tất cả các phần tử đều thoả mãn điều kiện thì trả về true còn ngược lại trả về false
```js
let array = [1, 2, 3, 4];
console.log(array.every(e => e > 0)) // trả về true
console.log(array.every(e => e > 3)) // trả về faslse
```

### 4: Hàm filter
Là hàm trả về một mảng mới các phần tử thoả mãn điều kiện đã đề ra
```js
let array = [1,2,3,4,5]
console.log(array.filter(e => e > 4)) // kết quả [5]
```

### 5: Hàm find()
Hàm find là hàm tìm kiếm phần tử đầu tiên trong mảng đã có thoả mãn một điều kiên gì đó
```js
let array = [1,2,3,4,5]
console.log(array.find(e => e > 3)) // => trả về 4
```

### 6: Hàm reduce
Là hàm để thực hiện một tác vụ nào đó lặp qua các phần tử. Hàm nhận vào function đầu với 2 tham số. 1 là tham số cần tính, 2 là các phần tử và thực hiện tác vụ trong hàm
 cái cuối là gia trị mặc định của hàm.
```js
let array = [1,2,3,4,5]
console.log(array.reduce((total, item)=> {return total + item}, 0))
```

### 7. Hàm findIndex
Là hàm tìm giá trị index(vị trí) đầu tiên thoả mãn điều kiện gì đó
```js
const array = [1, 2, 3, 4, 5]
console.log(array.findIndex(e => e > 4)) // Trả về giá trị 4 là vị trí của số 5 trong mảng
```

### 8. Hàm findLast
Là hàm tìm phần tử cuối cùng thoả mãn điều kiện nào đó
```js
const array = [1, 2, 3, 5, 4]
console.log(array.findLast(e => e > 2)) // Trả về giá trị là 4 tức là số cuối cùng thoả mãn dk gì đó
```

### 9. Hàm findLastIndex
Tương tự hàm findLast ở trên thì dưới này sẽ tìm vị trí index

### 10. Hàm forEach
Là hàm lặp qua từng phần tử không trả về gì hết, không trả về giá trị cũng không trả về mảng
```js
const array = [1, 2, 3, 5, 4]
console.log(array.forEach(item => console.log(item)))
```

### 11. Hàm includes()
Là hàm trả về giá trị bool xem mảng có chưa giá trị nào đó không
```js
const array = [1, 2, 3, 5, 4]
console.log(array.includes(3)) // trả về true tức là có chứa ohanaf tử đó
```

### 12. Hàm indexOf
Là hàm tìm vị trí của 1 phần từ
```js
const array = [1, 4, 2, 3, 5, 4]
console.log(array.indexOf(4, 2)) // Trả về 5
console.log(array.indexOf(4)) // Trả về 1 vị trí số 4 đầu
console.log(array.indexOf(9)) // Trả về -1 vì không có
```

### 13. Hàm join
Là hàm nối các phần tử với nhau thông qua kí tự nào đó
```js
const arrayName = ['minh', 'lung', 'linh']
console.log(arrayName.join('-')) // trả về minh-lung-linh
```

### 14. Hàm map
Là hàm lọc qua qua mảng và có trả về kết quả, có thể là một mảng mới
```js
const array = [1, 4, 2, 3, 5, 4]
const arrayNew = array.map((item, index) => (
  item * 2;
))
```

### 15. Hàm pop()
Là bỏ phần tử cuối cùng. Thay đổi trực tiếp mảng đó
```js
const array = ['A', 'B', 'D', 'C']
console.log(array.pop()) // trả về đáp án C
array.pop()
console.log(array) // trả về ['A', 'B', 'D']
```

### 16. Hàm push()
Thêm các giá trị vào cuối phần tử của mảng và không làm thay đổi mảng gốc

### 16. Hàm slice
Là hàm dùng cắt các phần tử của mảng
```js
array.slice(start, end)
```

### 17. Hàm splice
Có thể xoá các phàn tử hoặc thêm phần tử khác

# Phỏng vấn tạch ngày 26/08
### Câu 1: Phân biệt let var const
### Câu 2: Phân biệt undefined và null
### Câu 3: Xử lý bất đông bộ
### Câu 4: Hàm trong phần xử lý bất đồng bộ được gọi là hàm gì
### Câu 5: Phân biệt MVC và MVVM
### Câu 6: index trong postgree sql là gì
### Câu 7: Postgre khác gì mongodb khác gì sql
### Câu 8: having trong db là gì đi với cái gì và tác dụng làm gì
### Câu 9: Bọc try catch ngoài promise và ngoài async nếu lỗi thì trả về gì
- Bọc ngoài promisse thì ko trả về gì
- Trong async thì trả về lỗi
### Câu 10: Có mấy giai đoạn của promise
### Câu 11: https là gì
### Câu 12: Restful api là gì