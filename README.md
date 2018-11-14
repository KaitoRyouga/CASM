## Assembly : các lệnh cơ bản
> **_Thực hiện: Kaito ryouga_**
>
> **_Cập nhật lần cuối: 14/11/2018_**
----
###1.Lệnh NOP
>     Cú pháp lệnh:
    NOP
----
>     Tác dụng:

- Delay 1 chu kỳ máy

###2.Lệnh PUSH
>     Cú pháp lệnh:
    PUSH
----
>     Tác dụng:

- Cất dữ liệu vào ngăn xếp

###3.Lệnh POP
>     Cú pháp lệnh:
    POP
----
>     Tác dụng:

- Lấy dữ liệu ra khỏi ngăn xếp

###4.Lệnh CALL
>     Cú pháp lệnh:
     CALL [nhãn]
----
>     Tác dụng:

- Dùng để gọi một chương trình con, có thể là near hay far.

- Gọi chương trình con tại vị trí xác định bởi nhãn

###5.Lệnh RET
>     Cú pháp lệnh:
    RET [n]
----
>     Tác dụng:

- Dùng để kết thúc chương trình con, điều khiển sẽ được đưa về địa chỉ trước khi gọi chương trình con.

- Để kết thúc chương trình con dạng near và RETF dùng để kết thúc chương trình con dạng far.

- Trong trường hợp lệnh RET có hằng số n theo sau thì sẽ cộng với thanh ghi SP giá trị n (n phải là số chẵn). Lệnh này dùng để loại bỏ một số tham số chương trình con sử dụng ra khỏi stack.

###6.Lệnh Mov

>     Cú pháp lệnh:
    Mov      [Toán hạng đích], [Toán hạng nguồn]
----
>     Trong đó:

- [Toán hạng đích]: Có thể là thanh ghi (8 bít hay 16 bít), ô nhớ (chính xác hơn là địa chỉ của một ô nhớ) hay một biến nào đó. [Toán hạng đích] không thể là hằng số.   

- [Toán hạng nguồn]: Có thể là hằng số, biến, thanh ghi, ô nhớ (chính xác hơn là địa chỉ của một ô nhớ) nào đó.

>     Tác dụng:

- Lấy nội dung (giá trị) của [Toán hạng nguồn] đặt vào [Toán hạng đích]. Nội dung của [Toán hạng nguồn] không bị thay đổi.

###7.Lệnh Lea
>     Cú pháp lệnh:
    LEA     [Toán hạng đích],[Toán hạng nguồn]
----
>     Trong đó:

- [Toán hạng đích]: Là các thanh ghi 16 bít. [Toán hạng nguồn]: Là địa chỉ của một vùng nhớ hay tên của một biến.

>     Tác dụng:

- Lệnh LEA có tác dụng chuyển địa chỉ offset của [Toán hạng nguồn] vào [Toán hạng đích]. Lệnh này thường được sử dụng để lấy địa chỉ offset của một biến đã được khai báo trong chương trình. Thanh ghi được sử dụng trong trường hợp này là thanh ghi cơ sở (BX) và thanh ghi chỉ mục (SI và DI).   

###8.Lệnh Add và SUB
>     Cú pháp lệnh:
    Add       [Toán hạng đích],[Toán hạng nguồn]
    Sub       [Toán hạng đích],[Toán hạng nguồn]
----
>     Trong đó:

- [Toán hạng đích], [Toán hạng nguồn]: tương tự lệnh Mov.

>     Tác dụng:

- Lệnh Add (Addition): lấy giá trị/nội dung của [Toán hạng nguồn] cộng vào giá trị/nội dung của [Toán hạng đích], kết quả này đặt vào lại [Toán hạng đích]. 
- Lệnh Sub (Subtract): lấy giá trị/nội dung của [Toán hạng đich] trừ đi giá trị/nội dung của [Toán hạng nguồn], kết quả này đặt vào lại [Toán hạng đích].

### ***CHẠY THỬ VỚI CHƯƠNG TRÌNH C CÓ DÒNG LẶP FOR
'''
 
	int n,p=0,h=0,k=0,l=0;
	printf("so ky tu max cua day n la:");
	scanf("%d",&n);
	float a[20],t;
	for (int i=0;i<n;i++)
	{
		printf ("nhap a[%d]:",i);
		scanf("%f",&a[i]);	
	}
	float b[20],c[20];
	for (int i=0;i<n;i++)
	{
		if (a[i]>=0)
		{
			float x;
			x=a[i];
			b[k]=x;
			k++;
		}
		else 
		{
			float y;
			y=a[i];
			c[l]=y;
			l++;
		}
	}
	if (k!=0)
	{
	printf("mang so duong:");
	for (int i=0;i<k;i++)
	printf("%0.1f, ",b[i]);
	}
	if (l!=0)
	{
	printf("\nmang so am:");
	for (int j=0;j<l;j++)
	printf("%0.1f, ",c[j]);
	}
	getch();

'''
>     Kết quả thu được sau khi chạy x64dbg
----
>     Đang cập nhật.....
