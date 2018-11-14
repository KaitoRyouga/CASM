## Assembly : các lệnh cơ bản
>
> **_thực hiện: Kaito ryouga_**
>
> **_cập nhật lần cuối: 14/11/2018_**
>
----
###1.Lệnh NOP
- Lệnh này không thực hiện một công việc gì cả ngoại trừ việc tăng nội dung của thanh ghi EIP, nó không gây ra bất kì thay đổi nào trong thanh ghi, stack hoặc memory. 
- Chính vì ý nghĩa này của nó mà câu lệnh này thường được dùng vào mục đích hủy bỏ bất kì câu lệnh nào (không cho lệnh đó thực hiện), bằng cách ta thay thế câu lệnh sắp thực hiện bằng lệnh NOP chương trình sẽ vẫn thực thi nhưng thay vì thực thi câu lệnh gốc thì giờ đây do được thay thế bằng NOP nên nó sẽ không làm gì cả. 

###2.Lệnh PUSH

###3.Lệnh POP

###4.Lệnh CALL

###5.Lệnh RET

###6.Lệnh Mov

>     cú pháp lệnh:
		 Mov      [Toán hạng đích], [Toán hạng nguồn]
----
>
>     trong đó:
>

- [Toán hạng đích]: Có thể là thanh ghi (8 bít hay 16 bít), ô nhớ (chính xác hơn là địa chỉ của một ô nhớ) hay một biến nào đó. [Toán hạng đích] không thể là hằng số.   

- [Toán hạng nguồn]: Có thể là hằng số, biến, thanh ghi, ô nhớ (chính xác hơn là địa chỉ của một ô nhớ) nào đó.

>     tác dụng:
- Lấy nội dung (giá trị) của [Toán hạng nguồn] đặt vào [Toán hạng đích]. Nội dung của [Toán hạng nguồn] không bị thay đổi.

###7.Lệnh Lea

###8.Lệnh Add và SUB
