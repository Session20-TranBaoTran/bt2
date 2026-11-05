# SESSION 19 - EX02
# PHÂN TÍCH HIỆN TƯỢNG LỘ MẬT KHẨU VÀ BẢO VỆ TÀI KHOẢN

## 1. Phân tích hiện tượng Domino Effect

Trong tình huống này, tài khoản diễn đàn công nghệ của em bị hacker chiếm đoạt. Nguyên nhân là do em sử dụng chung một mật khẩu `123456` cho nhiều tài khoản như Gmail, Facebook và GitHub.

Khi hacker lấy được mật khẩu từ diễn đàn công nghệ, họ có thể thử sử dụng mật khẩu đó để đăng nhập vào các tài khoản khác của em.

Quá trình này được gọi là Credential Stuffing. Đây là hình thức tấn công sử dụng thông tin đăng nhập bị rò rỉ từ một website để thử đăng nhập vào nhiều website khác.

Ví dụ:

- Diễn đàn công nghệ bị hack và lộ mật khẩu `123456`.
- Hacker lấy được email và mật khẩu của em.
- Hacker thử dùng thông tin đó để đăng nhập Gmail.
- Sau đó tiếp tục thử đăng nhập Facebook và GitHub.
- Nếu các tài khoản đều sử dụng chung mật khẩu thì hacker có thể chiếm được nhiều tài khoản cùng lúc.

Hiện tượng này được gọi là Domino Effect vì chỉ cần một tài khoản bị lộ thông tin cũng có thể dẫn đến nhiều tài khoản khác bị chiếm đoạt.

## 2. Tại sao mật khẩu cảm tính dễ bị bẻ khóa?

Mật khẩu cảm tính thường được người dùng tự đặt dựa trên ngày sinh, tên, số điện thoại hoặc những dãy số dễ nhớ.

Ví dụ:

- 123456
- 12345678
- password
- 111111
- Ngày tháng năm sinh

Những mật khẩu này thường có quy luật đơn giản nên hacker có thể sử dụng các chương trình tự động để thử nhiều mật khẩu phổ biến.

Trong khi đó, mật khẩu do máy tính sinh ra thường có độ dài lớn và kết hợp nhiều loại ký tự như chữ hoa, chữ thường, số và ký tự đặc biệt.

Ví dụ:

Mật khẩu dễ đoán:

`123456`

Mật khẩu được tạo ngẫu nhiên:

`T9#mQ7!vL2@pX8`

Mật khẩu ngẫu nhiên khó đoán hơn vì không dựa trên những thông tin quen thuộc hoặc quy luật thông thường.

Vì vậy, em nên sử dụng mật khẩu dài, ngẫu nhiên và khác nhau cho từng tài khoản để hạn chế nguy cơ bị đánh cắp.

## 3. Tại sao nên sử dụng Password Manager?

Password Manager là công cụ giúp lưu trữ và quản lý mật khẩu tập trung. Thay vì phải ghi nhớ nhiều mật khẩu khác nhau, người dùng chỉ cần nhớ một mật khẩu chính gọi là Master Password.

Một số lợi ích của Password Manager:

- Tạo mật khẩu ngẫu nhiên và có độ bảo mật cao.
- Lưu trữ nhiều mật khẩu trong một nơi.
- Giảm tình trạng sử dụng chung một mật khẩu cho nhiều tài khoản.
- Hạn chế việc ghi mật khẩu ra giấy hoặc lưu trong các tệp văn bản không được bảo vệ.
- Giúp quản lý tài khoản thuận tiện hơn.

## 4. Giải thích cơ chế mã hóa AES-256

AES-256 là thuật toán mã hóa đối xứng sử dụng khóa có độ dài 256 bit. Đây là thuật toán được sử dụng trong nhiều hệ thống bảo mật dữ liệu.

Trong Password Manager, AES-256 có thể được sử dụng để mã hóa dữ liệu mật khẩu trước khi lưu trữ.

Quá trình hoạt động cơ bản:

Bước 1: Người dùng tạo Master Password để bảo vệ kho mật khẩu.

Bước 2: Password Manager sử dụng cơ chế tạo khóa từ Master Password để tạo khóa mã hóa.

Bước 3: Các mật khẩu được mã hóa bằng AES-256 trước khi lưu vào kho dữ liệu.

Bước 4: Khi người dùng nhập đúng Master Password, ứng dụng tạo lại khóa giải mã để đọc thông tin đã lưu.

Ví dụ:

Dữ liệu ban đầu:

`Facebook: MyPassword123`

Sau khi mã hóa, dữ liệu sẽ chuyển thành một chuỗi khó đọc nếu không có khóa giải mã phù hợp.

Điểm quan trọng là AES-256 sử dụng khóa mã hóa có độ dài 256 bit, giúp bảo vệ dữ liệu tốt nếu được triển khai đúng cách và khóa được quản lý an toàn.

## 5. So sánh Password Manager và ghi chép thủ công

| Tiêu chí | Ghi chép thủ công | Password Manager |
|---|---|---|
| Lưu trữ | Giấy hoặc sổ | Kho dữ liệu điện tử |
| Bảo mật | Dễ bị xem hoặc mất | Có thể mã hóa bằng AES-256 |
| Tạo mật khẩu | Thường tự nghĩ | Có công cụ tạo ngẫu nhiên |
| Quản lý | Khó quản lý nhiều mật khẩu | Quản lý tập trung |
| Tìm kiếm | Phải tìm từng ghi chép | Có thể tìm kiếm nhanh |

Theo