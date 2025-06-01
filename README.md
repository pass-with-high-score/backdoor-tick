# backdoor-tick

Idea: 

Ý tưởng của app đó là một **ứng dụng đồng hồ “ngụy trang”**. Khi mở lên, nó trông **chỉ như một app đồng hồ bình thường**, nhưng nếu người dùng **xoay kim đồng hồ đến một thời gian bí mật** (ví dụ như **3:14**), thì app sẽ **mở khóa một khu vực bí mật** – kiểu như **vault** – nơi người dùng có thể **giấu hình ảnh, video, tài liệu,…** bên trong một cách an toàn.

### 📱 Cách hoạt động:

1. **Mở app:** Giao diện giống y chang đồng hồ.
2. **Xoay kim giờ/phút đến “giờ bí mật”** (giả sử bạn cài là 3:14).
3. **App nhận diện đúng mã thời gian** → tự động mở phần **ẩn** chứa dữ liệu.
4. Có cả **PIN dự phòng** nếu quên mã giờ.
5. Mọi thứ được **mã hóa** để đảm bảo riêng tư.

### 🔐 Ý tưởng không mới nhưng khá thú vị:

* Đã có một số app tương tự như **Calculator Vault**, **Clock Vault**, v.v. — đều dùng chiêu “ngụy trang” để **giấu dữ liệu cá nhân**.
* Nhưng mà app này dùng cách **đặt giờ bí mật** thay vì giao diện máy tính, nên cũng có nét riêng.


* Giao diện analog clock (có kim xoay thật).
* Logic nhận dạng giờ (so sánh `hour` + `minute` với mã bí mật).
* Navigation đến vault khi đúng giờ.
* Mã hóa/giải mã file bằng thư viện như **Tink** hoặc **Cipher** trong Android SDK.

