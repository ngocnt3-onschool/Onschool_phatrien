
# Công cụ tự động xây dựng OSP100 - GKV100

Được sử dụng để tự động xây dựng bản đặt hàng course OSP100 

+ Ngôn ngữ sử dụng: Google Apps Script
+ Giảm thiểu các tác vụ tay chân, thời gian thực hiện. Tăng hiệu suất công việc và tính chính xác (độ chính xác 100% thay vì các lỗi thao tác khi làm thủ công)


## Cài đặt

Đối với mỗi tài khoản Mail lần đầu sử dụng Tool, khi click **button** sẽ hiện ra pop-up "Ủy quyền". 
Khi xuất hiện pop-up cần click "ủy quyền" cho tool sử dụng dữ liệu. 
Chỉ cần cấp quyền 1 lần duy nhất. Từ sau sử dụng sẽ không cần "Ủy quyền" lại nữa.


    
## Input

Mỗi UNI sẽ được cung cấp một link duy nhất như sau : 

![Tool](https://i.ibb.co/gMQYHMYB/Screenshot-2025-06-03-152550.png)

## Cấu Trúc 

![Cấu trúc](https://i.ibb.co/BH8QfZsx/z6667740881614-889497db4950218b699621e661f1b2ae.jpg)

**1. GK1000....**
 Đây là sheet được đặt GK1000 làm **input 1** cho tool.
 
 + Nhân sự sử dụng cần lấy đúng GK1000 đang ban hành đưa vào để sử dụng. 
 + Không sửa xóa các nội dung có trên GK1000, tránh việc sai form gây lỗi tool.
 + GK1000 được GKV ban hành đã được làm chuẩn hóa form để có thể sử dụng cùng tool.



**2. SLSV**

![SLSV](https://i.ibb.co/v6s57D3y/Screenshot-2025-06-03-155930.png)
Đây là sheet về số lượng sinh viên tại các class code A. Được sử dụng làm **input 2** cho tool.

+ Nhân sự cần bổ sung đầy đủ các **class code A** có trạng thái **GK_ready** để sử dụng.
+ SLSV cần lấy đúng theo **P835** hoặc theo **F111** trạng thái L8

**3. Thống kê**

![Thống kê](https://i.ibb.co/Fby2b217/Screenshot-2025-06-03-163312.png)
Đây là sheet tool tạo ra nhằm mục đích kiểm soát và quản trị OSP 

**Đợt học:** Các đợt học có trong GK1000 và được link với sheet OSP100 đã được tạo bởi tool

+ Nhân sự click vào đợt học cần sử dụng và sẽ tự nhảy đến sheet OSP đã tạo.
+ OSP đã tạo theo form chuẩn của TOL và có thể sử dụng để đặt hàng luôn, không cần chỉnh sửa gì thêm.

**Tháng học:** Tháng học của đợt học

**Năm học:** Năm học của đợt học

--> Đợt học đã được tự động sắp xếp theo thời gian từ trên xuống

**Số course:** Số lượng course của OSP100

**Ngày đặt hàng:** Dữ liệu ngày đặt hàng được tự tạo theo timeline trong quy trình vận hành OSP của từng trường

**Ngày đặt hàng thực tế:** Nhân sự cần điền ngày thực tế đặt hàng tại đây

**Ngày trả hàng:** Dữ liệu ngày trả hàng được tự tạo theo timeline trong quy trình vận hành OSP của từng trường

**Ngày trả hàng thực tế:** Nhân sự cần điền ngày thực tế trả hàng của TOL tại đây

**4. OSP100**

![OSP100](https://i.ibb.co/svHKrWkc/Screenshot-2025-06-03-164218.png)
Các OSP100 được tạo bởi tool.

## Hướng dẫn sử dụng

Nhân sự cần phải đảm bảo **Input 1 và Input 2** như trên.

**Step 1: Button**

![button](https://i.ibb.co/9HhZHrWF/Screenshot-2025-06-03-160822.png)

+ Nhân sự click button "GKV-ONSCHOOL phát triển" -> "Chạy cập nhật dữ liệu" để thực hiện chạy tool.
+ Button được thêm vào thanh công cụ của Gg-sheet


**Step 2: Pop-up**
Cửa sổ pop-up sẽ hiện ra cùng với dòng trạng thái đang chạy như sau: 

![Pop-up](https://i.ibb.co/67x1FpW1/Screenshot-2025-06-03-161322.png)

Click "OK" để hoàn thành việc đồng ý chạy tool. 

Click "Hủy" hoặc "loại bỏ" để hoàn tác chạy tool.

**Step 3: Chạy tool**

Tool chạy sẽ có 2 phase:

**- Phase 1 :** Tool sẽ xóa hết tất cả các OSP đã tạo. Bao gồm cả các sheet dư thừa. Chỉ để lại 2 sheet Input. 

*Lưu ý: Nhân sự cần tạo bản sao OSP tại thời điểm trước khi chạy tool nếu cần cho việc so sánh osp của GK1000 cũ khi có sự vụ*


**- Phase 2 :** Tạo các OSP100

Tool sẽ chạy khởi tạo tất cả OSP100 cho tất cả các ngày bắt đầu có trong GK1000.

![Phase 2](https://i.ibb.co/pr2qZB71/chay2.gif)

**Step 4: Hoàn thành**

Sau khi tool chạy xong sẽ hiển thị ra pop-up như sau: 

![hoanthanh](https://i.ibb.co/hJbVZX17/Screenshot-2025-06-03-165408.png)

Click "Ok" để hoàn tất quá trình và đã có thể sử dụng.
