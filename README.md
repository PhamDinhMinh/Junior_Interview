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
## Câu 2: 
Redux saga hoạt động?
Redux, zustand có cơ chế presit không ( là cái lưu lại khi out khỏi app )
## Câu3: 
Cấu hình firebase
## Câu4: lifecycle hoạt động ra sao
## Câu5: 
- Nếu ko dùng react query thì có thể dùng gì gọi api(useEff)
- Xử lý bất đồng bộ ntnt
## Câu 6: Từng đẩy app lên chpaly chưa
## Câu 7: Dùng gì để điều hướng các màn hình, truyền dữ liệu trong react navigation như thế nào
## Câu 8: useRef dùng như nào
## Câu 9: Câu hỏi về authen token. Khi token hết hạn e refetch token thì chủ yếu làm gì
- Tạo token mới 
## Câu 10: Liên quan về git