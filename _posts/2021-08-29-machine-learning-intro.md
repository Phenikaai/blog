---
layout: post
title: Machine Learning là gì?
subtitle: Các định nghĩa khác nhau về Machine Learning
date:       2021-08-29 8:00:00
author:     "Mai Xuan Trang"
background: '/img/posts/07.jpg'
---

Chúng ta đã nghe rất nhiều về "<b>Machine Learning</b>" (<b>Học máy</b> hoặc <b>Máy học</b>), đặc biệt là những năm gần đây "Machine Learning" đang trở thành topic "hot" nhất không chỉ trong nghiên cứu mà trong cả industry. Vậy "Machine Learning" là gì mà nó lại trở nên nổi tiếng như vậy, bài viết này thảo luận một số định nghĩa về "Machine Learning" từ những góc nhìn khác nhau. Bài viết cũng cung cấp các thông tin về tài nguyên để bạn bắt đầu tìm hiểu về Machine Learning.

## Các định nghĩa chuẩn (Standard Definitions)

Dưới đây tôi đưa ra một số định nghĩa về "Machine Learning" từ bốn quyển sách nổi tiếng thường hay được dùng để giảng day trong các trường đại học nổi tiếng. Những cuốn sách này được xem như là kinh thánh trong Machine Learning. Tôi chọn bốn định nghĩa để làm nổi bật một số quan điểm hữu ích trong trong lĩnh vực này.

### Mitchell's Machine Learning

Quyển sách nổi tiếng về [Machine Learning](https://www.amazon.com/dp/0070428077?tag=mllog-20) của Tom Mitchell đưa ra một định nghĩa ngay đầu tựa đề quyển sách:

>💡 *The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.*

Định nghĩa này ngắn gọn và dễ hiểu, theo định nghĩa này thì công việc của Machine Learning là tạo ra các chương trình máy tính có thể tự động cải thiện thông qua những kinh nghiệm chúng đã trải qua.

Cũng trong quyển sách này, ở phần giới thiệu Mitchell đưa ra một công thức mà rất hay được sử dụng trong Machine Learning:

>💡 *A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E.*

### Elements of Statistical Learning

Quyển sách thứ hai tôi muốn đề cập đến là cuốn: [The Elements of Statistical Learning: Data Mining, Inference, and Prediction](https://www.amazon.com/dp/0387848576?tag=mllog-20) được viết bở ba nhà thống kê (statisticians) từ Standford. Trong phần tựa đề của cuốn sách có viết:

>💡 *Vast amounts of data are being generated in many fields, and the statisticians’ job is to make sense of it all: to extract important patterns and trends, and to understand “what the data says”. We call this learning from data.*

Dưới góc nhìn của các nhà thống kê, Machine Learning là dùng các công cụ thống kê để giải thích dữ liệu trong một ngữ cánh nào đấy. Trong cuốn sách này các tác giả giải thích tất cả các lĩnh vực của Machine Learning. (Một quyển sách phải đọc cho những ai muốn bước chân vào lĩnh vực Machine Learning).

### Pattern Recognition

Trong quyển [Pattern Recognition and Machine Learning](http://www.amazon.com/dp/0387310738?tag=mllog-20), Bishop viết trong tựa đề của quyển sách:

>💡 *Pattern recognition has its origins in engineering, whereas machine learning grew out of computer science. However, these activities can be viewed as two facets of the same field*

Định nghĩa này là từ góc nhìn engineering (engineering perspective). Đây là một phương pháp tiếp cận đã được dùng trong thời gian dài, đáng để chung ta học theo. Theo một nghĩa rộng hơn, bất kể một phương pháp trong một lĩnh vực nào đó, nếu phương pháp đó phù hợp với điều chúng ta cần là giúp chúng ta có được kết quả từ việc học từ dữ liệu, thì chúng ta có thể gọi phương pháp đó là Machine Learning.

### An Algorithmic Perspective
Trong cuốn [Machine Learning: An Algorithmic Perspective](http://www.amazon.com/dp/B005H6YE18?tag=mllog-20), Marsland đưa ra định nghĩa dựa trên định nghĩa của Mitchel:

>💡 *One of the most interesting features of machine learning is that it lies on the boundary of several different academic disciplines, principally computer science, statistics, mathematics, and engineering. …machine learning is usually studied as part of artificial intelligence, which puts it firmly into computer science …understanding why these algorithms work requires a certain amount of statistical and mathematical sophistication that is often missing from computer science undergraduates.*

Định nghĩa này rất sau sắc và mang nhiều thông tin. Điều đầu tiên Marsland nhấn mạnh tính chất đa lĩnh vực của Machine Learning từ khoa học máy tính, xác suất thông kê, toán và kỷ thuật. Tác giả cũng nhấn mạnh rằng để hiểu được các thuật toán trong Machine Learning chúng ta cần có lượng kiến thúc nhất định về thông kê và toán học, các kiến thức này thì các sinh viên đại học hiện còn rất hạn chế. Vậy bạn muốn bước chân vào Machine Learning, hãy bắt đầu chuẩn bị cho mình những kiến thức nền tảng về toán và xác suất thông kê.

### Biển đồ Venn

Chúng ta có thể thấy rõ hơn các lĩnh vực và kỷ năng cần thiết cho Machine Learning trong [biểu đồ Venn](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram) tạo bởi Drew Coway dưới đây:

{% include image.html
            img="img/posts/Data_Science_VD.png"
            title="Data science diagram"
            caption="Data science Venn diagram by Drew Coway"
            url="http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram"%}

Trong biểu đồ Venn này, Coway mô tả những người có kỷ năng hack và có chuyên môn là những người "nguy hiểm" (Thuộc Danger Zone!). Những người này có thể truy nhập và cấu trúc dữ liệu, họ biết lĩnh vực họ đang làm và có thể chạy những phương pháp và trình bày kết quả, tuy nhiên họ họ không hiểu ý nghĩa của những kết quả đó. Để hiểu về những kết quả đấy họ cần thêm những kiến thức về toán học và xác suất thông kê.

## Resources: Để bạn bắt đầu với Machine Learning

Trong bài viết này tôi đã đề cập đến một vài tài nguyên hữu ích để nghiên cứu về Machine Learning. Tôi liệt kê lại dưới đây:

### Books

Dưới đây là bốn quyển "kinh thánh" trong Machine Learning, bạn nên đọc những cuốn này nếu muốn dân thân vào lĩnh vực khó khăn nhưng đầy thú vị này.

* [Machine Learning](https://www.amazon.com/dp/0070428077?tag=mllog-20) của Mitchell
* [The Elements of Statistical Learning: Data Mining, Inference, and Prediction](https://www.amazon.com/dp/0387848576?tag=mllog-20) của Hastie, Tibshirani và Friedman
* [Pattern Recognition and Machine Learning](http://www.amazon.com/dp/0387310738?tag=mllog-20) của Bishop
* [Machine Learning: An Algorithmic Perspective](http://www.amazon.com/dp/B005H6YE18?tag=mllog-20) của Marsland.

Ngoài ra Drew Conway và John Myles White cũng viết một cuốn rất thú vị và thiên về thực hành nhiều hơn: [Machine Learning for Hackers](http://www.amazon.com/dp/1449303714?tag=mllog-20).

### Các trang Q&A

Bạn cũng nên tham gia vào các Q&A websites, có rất nhiều thảo luận thú vị về Machine Learning, dưới đây là một số ví dụ:

- **Quora**: [What is machine learning in layman's terms](https://www.quora.com/What-is-machine-learning-in-laymans-terms-1?redirected_qid=1155077), [What is data science?](https://www.quora.com/Data-Science/What-is-data-science)
- **Cross Validated**: [The Two Cultures: statistics vs. machine learning?](http://stats.stackexchange.com/questions/6/the-two-cultures-statistics-vs-machine-learning)
- **Stack Overflow**: [ What is machine learning?](http://stackoverflow.com/questions/2620343/what-is-machine-learning)