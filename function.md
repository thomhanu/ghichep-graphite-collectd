###Mục lục

[Mở đầu](#modau)

[1. Sum function](#sum)
- [1.1 Mô tả](#motasum)
- [1.2 Minh họa](#minhhoasum)

[2. Average function](#average)
- [2.1 Mô tả](#motaaverage)
- [2.2 Minh họa](#minhhoaaverage)

[3. Product function](#product)
- [3.1 Mô tả](#motaproduct)
- [3.2 Minh họa](#minhhoaproduct)

[4. Min value function](#minvalue)
- [4.1 Mô tả](#motaminvalue)
- [4.2 Minh họa](#minhhoaminvalue)

[5. Max value function](#maxvalue)
- [5.1 Mô tả](#motamaxvalue)
- [5.2 Minh họa](#minhhoamaxvalue)

[6. Difference function](#difference)
- [6.1 Mô tả](#motadifference)
- [6.2 Minh họa](#minhhoadifference)

[7. Ratio function](#ratio)
- [7.1 Mô tả](#motaratio)
- [7.2 Minh họa](#minhhoaratio)

[8. Maximum value above function](#maxabove)
- [8.1 Mô tả](#motamaxabove )
- [8.2 Minh họa](#minhhoamaxabove)

[9. Maximum value below function](#maxbelow)
- [9.1 Mô tả](#motamaxbelow)
- [9.2 Minh họa](#minhhoamaxbelow)

[10. Minimum value above function](#minabove)
- [10.1 Mô tả](#motaminabove)
- [10.2 Minh họa](#minhhoaminabove)

[11. Color function](#color)
- [11.1 Mô tả](#motacolor)
- [11.2 Minh họa](#minhhoacolor)

[12. Summarize function](#summarize)
- [12.1 Mô tả](#motasummarize)
- [12.2 Minh họa](#minhoasummarize)

[13. Highest Average Value Function](#highestaverage)
- [13. 1 Mô tả](#motahighestaverage)
- [13.2 Minh họa](#minhhoaaverage)

[14. Draw in Second Y Axis](#secondy)
- [14.1 Mô tả](#motasecondy)
- [14.2 Minh họa](#minhhoasecondy)

[15. Average Value Above](#averageabove)
- [15.1 Mô tả](#motaaverageabove)
- [15.2 Minh họa](#minhhoaaverageabove)

[16. Average Value Below](#averagebelow)
- [16.1 Mô tả](#motaaveragebelow)
- [16.2 Minh họa](#minhhoaaveragebelow)

<a name="modau"></a>
#### Mở đầu.

Function được sử dụng để chuyển đổi, kết hợp và thực hiện các tính toán trên chuỗi dữ liệu. Chức năng này được áp dụng bằng cách sử dụng giao diện Composer hoặc bằng cách điều khiển các thông số mục tiêu trong Render API.

<a name="sum"></a>
#### 1. Sum function.

<a name="motasum"></a>
#####1.1 Mô tả.
- Function sum giúp người dùng tính tổng các thông số được chọn

<a name="minhhoasum"></a>
#####1.2 Minh họa.

- Người dùng chọn thông số muốn tính tổng. Ở đây tôi chọn memory: used, buffered, userd và free. Sau đó chọn Apply Fuction-> Combine-> Sum.

Hình 1
![sum](/images/functionSum1.png)

Hình 2
![sum](/images/functionSum2.png)

Chú ý: Trong đó sumSeries(collectdServer.memory.memory-buffered,collectdServer.memory.memory-cached,collectdServer.memory.memory-free,collectdServer.memory.memory-used)= total RAM = cached + used + buffered+ free= 1024 M
<a name="average"></a>
####2. Average function.

<a name="motaaverage"></a>
#####2.1 Mô tả.
- Funtion average giúp người dùng tính trung bình thông số được chọn.

<a name="minhhoaaverage"></a>
#####2.2 Minh họa.

- Người dùng chọn các thông số muốn tính trung bình. Ở đây tôi chọn packet nhận và chuyển đi trên card eth0. Sau đó chọn Apply Fuction-> Combine-> Average.

Hình 3
![average](/images/functionAverage1.png)

Hình 4
![average](/images/functionAverage2.png)

Chú ý: Trong đó averageSeries(collectdServer.interface-eth0.if_packets.tx,collectdServer.interface-eth0.if_packets.rx)=(số packet nhận + số packet truyền ra ngoài)/2

<a name="product"></a>
####3. Product function.

<a name="motaproduct"></a>
#####3.1 Mô tả.
- Product function giúp người nhân hai thông số được chọn với nhau.

<a name="minhhoaproduct"></a>
#####3.2 Minh họa.

- Người dùng chọn hai thông số. Ở đây tôi chọn load.shortterm và load.longterm. Sau đó chọn Apply Fuction-> Combine-> Product.

Hình 5
![average](/images/functionProduct1.png)

Hình 6
![average](/images/functionProduct2.png)

Chú ý: Trong đó multiplySeries(collectdServer.load.load.shortterm,collectdServer.load.load.longterm)= 0.12 x 0.14 = 0.0168

<a name="minvalue"></a>
####4. Min value function.

<a name="motaminvalue"></a>
#####4.1 Mô tả.

- Min value function giúp người dùng tìm ra chỉ thông số nào là thấp nhất trong các thông số được chọn. Hệ thống sẽ so sánh các điểm để tìm ra thông số nhỏ nhất.

<a name="minhhoaminvalue"></a>
#####4.2 Minh họa

- Chọn các thông số người dùng muốn so sánh. Ở đây tôi chọn memory: free, used, cached và buffered. Sau đó chọn Apply Fuction-> Combine-> Min value.

Hình 7
![minvalue](/images/functionMinvalue1.png)

Hình 8
![minvalue](/images/functionMinvalue2.png)

Trong trường họp này Min value là buffered memory.

<a name="maxvalue"></a>
####5. Max value function.

<a name="motamaxvalue"></a>
#####5.1 Mô tả.

- Min value function giúp người dùng tìm ra chỉ thông số nào là cao nhất trong các thông số được chọn. Hệ thống sẽ so sánh các điểm để tìm ra thông số lớn nhất.

<a name="minhhoamaxvalue"></a>
#####5.2 Minh họa

- Chọn các thông số người dùng muốn so sánh. Ở đây tôi chọn memory: free, used, cached và buffered. Sau đó chọn Apply Fuction-> Combine-> Max value.

Hình 9
![maxvalue](/images/functionMaxvalue1.png)

Hình 10
![maxvalue](/images/functionMaxvalue2.png)

Ở đây Max value là free memory.

<a name="difference"></a>
####6. Difference function.

<a name="motadifference"></a>
#####6.1 Mô tả.

- Người dùng có thế so sánh giữa hai thông số được chọn. Lấy thông số chọn đầu tiên trừ cho thông số thứ hai được chọn.

<a name="minhhoadifference"></a>
#####6.2 Minh họa.

- Chọn hai thông số người dùng muốn so sánh. Tôi chọn packet nhận và truyền đi của card eth0. Sau đó chọn Apply Function-> Calculate-> Difference.

Hình 11
![difference](/images/functionDifference1.png)

Hình 12
![difference](/images/functionDifference2.png)

Có thể thấy rằng số lượng packet transform nhỏ hơn số lượng packet recieve


<a name="ratio"></a>
####7. Ratio function.

<a name="motaratio"></a>
#####7.1 Mô tả.

- Ratio function giúp người dùng có thể biết tỉ lệ giữa hai thông số được chọn.

<a name="minhhoaratio"></a>
#####7.2 Minh họa.

- Chọn 2 function người dùng muốn so sánh. Tôi so sánh dung lượng của free và used trong memory.

Chọn hai thông số đó-> Apply Function-> Calculate-> Ratio.

Hình 13
![ratio](/images/functionRatio1.png)

Hình 14
![ratio](/images/functionRatio2.png)

Chú ý: Nhìn vào biểu đồ người dùng có thể nhận thấy rằng dung lượng free luôn lớn hơn dung lượng used trong memory. Lấy free chia cho used kết quả luôn là lớn hơn 1.

<a name="maxabove"></a>
####8. Maximum value above function.

<a name="motamaxabove"></a>
##### 8.1 Mô tả.

- Giúp người dùng lọc ra những thông số có giá trị lớn nhất trên một mức nào đó. 

<a name="minhhoamaxabove"></a>
#####8.2 Minh họa

- Chon load.longterm và load.shortterm -> Apply Function -> Filter -> Maximum value above.

Hình 15
![maxabove](/images/functionmaxabove1.png)

Sau đó, người dùng được yêu cầu điền vào một giá trị, giá trị này để so sánh với giá trị lớn nhất của longterm và shortterm. Nếu giá trị lớn nhất của longterm và shortterm nhỏ hơn giá trị này thì longterm và shortterm sẽ không được biểu diễn trên biểu đồ. Còn nếu lớn hơn thì chúng vẫn giữ nguyên. 
Ở đây, tôi điền vào giá trị là 0.17

Hình 16

![maxabove](/images/functionmaxabove2.png)

Biểu đồ ban đầu:

Hình 17
![maxabove](/images/functionmaxabove3.png)

Biểu đồ sau khi thực hiện function maximum value above. Chỉ còn load.longterm trên biểu đồ.

Hình 18
![maxabove](/images/functionmaxabove4.png)

<a name="maxbelow"></a>
####9. Maximum value below.

<a name="motamaxbelow"></a>
#####9.1 Mô tả.

- Maximum value below giúp người dùng lọc ra những thông số có giá trị lớn nhất nhỏ hơn một mức nào đó.

<a name="minhhoamaxbelow"></a>
#####9.2 Minh họa.

- Tương tự như maximum value above function. Chon load.longterm và load.shortterm -> Apply Function -> Filter -> Maximum value below.

Hình 19
![maxbelow](/images/functionmaxbelow1.png)

- Sau đó, người dùng được yêu cầu điền vào một giá trị, giá trị này để so sánh với giá trị lớn nhất của longterm và shortterm. Nếu giá trị lớn nhất của longterm và shortterm lớn hơn giá trị này thì longterm và shortterm sẽ không được biểu diễn trên biểu đồ. Còn nếu nhỏ hơn thì chúng vẫn giữ nguyên. 
Ở đây, tôi điền vào giá trị là 0.2

Hình 20

![maxbelow](/images/functionmaxbelow2.png)

Biểu đồ ban đầu:

Hình 21
![maxbelow](/images/functionmaxbelow4.png)

Biểu đồ sau khi thực hiện function maximum value below. Chỉ còn load.longterm trên biểu đồ, vì maximum của load.longterm=0.15 <0.2

Hình 22
![maxbelow](/images/functionmaxbelow3.png)

<a name="minabove"></a>
####10. Minimum value above function.

<a name="motaminabove"></a>
#####10.1 Mô tả.

- Minimum value above giúp người dùng lọc ra những thông số có giá trị nhỏ nhất lớn hơn một mức nào đó.

<a name="minhhoaminabove"><a/>
#####10.2 Minh họa.

- Chon load.longterm và load.shortterm -> Apply Function -> Filter -> Minimum value above.

Hình 23
![minabove](/images/functionminabove1.png)

Sau đó, người dùng được yêu cầu điền vào một giá trị, giá trị này để so sánh với giá trị nhỏ nhất của longterm và shortterm. Nếu giá trị nhỏ nhất của longterm và shortterm nhỏ hơn giá trị này thì longterm và shortterm sẽ không được biểu diễn trên biểu đồ. Còn nếu lớn hơn thì chúng vẫn giữ nguyên. 
Ở đây, tôi điền vào giá trị là 0.1

Hình 24

![minabove](/images/functionminabove2.png)

Biểu đồ ban đầu:

Hình 25
![minabove](/images/functionminabove3.png)

Biểu đồ sau khi thực hiện function minium value above. Chỉ còn load.longterm trên biểu đồ, vì miniimum của load.longterm >0.1

Hình 26
![minabove](/images/functionminabove4.png)

<a name="color"></a>
####11. Color function.

<a name="motacolor"></a>
##### 11.1 Mô tả

Color function giúp người dùng có thể đánh dấu được thông số muốn theo dõi.

<a name="minhhoacolor"></a>
#####11.2 Minh họa

Chọn một thông số cụ thể, ở đây tôi chọn memory free -> Apply Function -> Special -> Color

Hình 27
![color](/images/functioncolor1.png)

Sau đó người dùng được yêu cầu nhập màu sắc mà họ muốn thông số được chọn hiện thị, ở đây tôi chọn màu đen.

Hình 28

![color](images/functioncolor2.png)

Chú ý: Người dùng có thể điền màu hoặc mã của màu sắc đó.

Biểu đồ ban đầu:

Hình 29
![color](/images/functioncolor3.png)

Biểu đồ sau khi áp dụng function color:

Hình 30
![color](/images/functioncolor4.png)

<a name="summarize"></a>
####12. Summarize funtion

<a name="motasummarize"></a>
#####12.1 Mô tả 

Summarize funtion giúp người dùng có thể chuyển đổi dữ liệu theo một quy mô nhỏ hơn theo thời gian. 
Ví dụ: nếu trung ta có các dữ liệu được thể hiện trong vài phút, ta có thể nhóm dữ liệu theo giờ bằng summarize function

<a name="minhhoasummarize"></a>
#####12.2 Minh họa

Chọn thông số -> Apply Function -> Transform -> Summarize

Hình 31
![summarize](/images/functionSummarize1.png)

Người dùng được yêu cầu điền thời gian muốn chuyển đổi, ở đây tôi chọn 1h

Hình 32

![summarize](/images/functionSummarize2.png)

Biểu đồ ban đầu:

Hình 33
![summarize](/images/functionSummarize4.png)

Biểu đồ sau khi áp dụng function Summarize:

Hình 34
![summarize](/images/functionSummarize3.png)

Chú ý: Khi áp dụng function này, "sum" được dùng là hàm mặc định được áp dụng. Thay vì sử dụng "sum" người dùng cũng có thể dùng avg, min và max.

Để áp dụng avg, min, max người dùng có thể làm theo hai cách sau:

Cách 1: 

Hình 35

![summarize](/images/functionSummarize5.png)

Hình 36
![summarize](/images/functionSummarize6.png)

Cách 2: Sau khi người dùng đã áp dụng function Summarize và muốn thay đổi hàm sum thành hàm avg:

Hình 37

![summarize](/images/functionSummarize7.png)

Hình 38

![summarize](/images/functionSummarize8.png)

Hình 39

![summarize](/images/functionSummarize9.png)

Hình 40
![summarize](/images/functionSummarize10.png)

<a name="highestavergae"></a>
####13. Highest Average Value function

<a name="motahighestaverage"></a>
#####13.1 Mô tả

Trong những trường hợp người dùng có nhiều metric, người dùng chỉ muốn đồ thị hiển thị 5 hoặc 10 metric thích hợp, người dùng có thể sử dụng function highestAverage.
Với chức năng này, graphite sẽ rút ra những số liệu có trung bình lớn nhất.

<a name="minhhoaaverage"></a>
#####13.2 Minh họa

Chọn thông số -> Apply function -> Filter -> Highest Average Value

Hình 41
![highestaverage](/images/functionHighestaverage1.png)

Hình 42

![highestaverage](/images/functionHighestaverage2.png)

Chú ý: Các function tương tự: highestCurrent, highestMax, lowestAverage, lowestCurrent.


<a name="secondy"></a>
####14. Draw in Second Y Axis

<a name="motasecondy"></a>
#####14.1 Mô tả

Function này giúp người dùng có thể hiện thị thêm một cột Y trên biểu đồ. Khi người dùng muốn quan sát hai thông số với 2 đơn vị khác nhau người dùng có thể dùng function này.

<a name="minhhoasecondy"></a>
#####14.2 Minh họa

Chọn thông số -> Apply Function -> Special -> Draw in Second Y Axis

Hình 43
![sencondy](/images/functionsecondY1.png)

Biểu đồ ban đầu:

Hình 44
![sencondy](/images/functionsecondY2.png)

Biểu đồ sau khi áp dụng function Draw in Sencond Y Axis:

Hình 45
![sencondy](/images/functionsecondY3.png)

<a name="averageabove"></a>
####15. Average Value Above

<a name="motaaverageabove"></a>
#####15.1 Mô tả

Average Value Above function giúp người dùng lọc ra những thông số có giá trị trung bình lớn hơn một giá trị nào đó.

<a name="minhhoaaverageabove"></a>
#####15.2 Minh họa

Chọn thông số -> Apply Function -> Filter -> Average Value Above.

Hình 46
![averageabove](/images/functionAverageabove1.png)

Hình 47

![averageabove](/images/functionAverageabove2.png)

Biểu đồ ban đầu:

Hình 48
![averageabove](/images/functionAverageabove3.png)

Biểu đồ sau khi áp dụng Average Value Above function

Hình49
![averageabove](/images/functionAverageabove4.png)

Chú ý: Số lượng packet receive và transfer trên card eth0 không xuất hiện trên biểu đồ vì trung bình của 2 thông số này nhỏ hơn 50.

<a name="averagebelow"></a>
####16. Average Value Below

<a name="motaaveragebelow"></a>
#####16.1 Mô tả

Average Value Below function giúp người dùng lọc ra những thông số có giá trị trung bình nhỏ hơn một giá trị nào đó.

<a name="minhhoaaveragebelow"></a>
#####16.2 Minh họa

Chọn thông số -> Apply Function -> Filter -> Average Value Above.

Hình 50
![averagebelow](/images/functionAveragebelow1.png)

Hình 51

![averagebelow](/images/functionAveragebelow2.png)

Biểu đồ ban đầu:

Hình 52
![averagebelow](/images/functionAveragebelow4.png)

Biểu đồ sau khi áp dụng Average Value Below function

Hình53
![averagebelow](/images/functionAveragebelow3.png)

Chú ý: Các thông số của memory không xuất hiện trên biểu đồ vì trung bình của những thông số này lớn hơn 10.

## Link Tham Khảo

https://graphite.readthedocs.org/en/0.9.10/functions.html
