# An Introduction to JavaScript 1

Hãy cùng xem xem có gì đặc biệt ở JavaScript, chúng ta có thể làm gì dể nắm thóp được nó, và những công nghệ khác mà ta có thể sử dụng nó dựa trên JavaScript

## What is JavaScript?

*JavaScript* đã được tạo ra ban đầu là dùng để "làm nên 1 cái trang web".

Cái trương trình trong ngôn ngữ này đc gọi là *scripts*. Nó có thể được viết dưới dạng HTML của trang web và sẽ chạy ngay sau khi trang web mở/tải.

Scripts được cung cấp và thực hiện dưới dạng văn bản thô/ văn bản thần tuý/ cổ điển . Nó không cần sự chuẩn bị hoặc biên soạn đặc biệt để có thể chạy.

Trong phương diện này, JavaScript rất khác biệt so với một loại ngôn ngữ lập trình khác tên [Java](https://en.wikipedia.org/wiki/Java_(programming_language)).

```smart header="Why is it called JavaScript?"
Khi JavaScript mới được tạo ra, tên của nó là: "LiveScript". nhưng khi đó Java rất là nổi tiếng, nên họ đã lựa chon đặt cái ngôn cữ này ở vị trí "em trai" của Java sẽ giúp ích.

Nhưng đông thời với việc nó ngày càng lớn mạnh, JavaScript trở thành 1 ngôn ngữ độc lập và có tên gọi riêng của nó [ECMAScript](http://en.wikipedia.org/wiki/ECMAScript), và bây giờ nó không còn quan hệ nào với Java.
```

Cho đến ngày nay, JavaScript không chỉ để lầm web, mà còn được đùng để làm các server, hoặc một thiết bị có cái trương trình đặc biệt tên [the JavaScript engine](https://en.wikipedia.org/wiki/JavaScript_engine).

Cái trang web giờ đã có 1 bộ máy riêng gọi là "JavaScript virtual machine".

Mỗi 1 cái engine sẽ có 1 cái "codenames" khác nhau. For example:

- [V8](https://en.wikipedia.org/wiki/V8_(JavaScript_engine)) -- in Chrome, Opera and Edge.
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) -- in Firefox.
- ...There are other codenames like "Chakra" for IE, "JavaScriptCore", "Nitro" and "SquirrelFish" for Safari, etc.

những cái ví dụ trên khá là quan trọng vì chúng đã đc sử dụng bởi những coder trên internet. Chúng ta cũng sẽ dùng nó, lấy ví dụ, nếu "Một tính năng X được hỗ trợ bởi engine V8", Suy ra, nó có thể chạy đc ở chrome, opera và edge.

```smart header="How do engines work?"

Engines rất phức tạp. nhưng cái cơ bản rất dễ.

1. The engine (embedded nếu ở trong cái browser) đọc ("phân tích") cái script.
2. sau đó nó chuyển đổi ("biên dịch") cái script thành machine code.
3. Và cái mã máy này chạy khá nhanh khi nó được chạy.

Cái engine sẽ tối ưu hoá mỗi bước trong quá trình. khi nó chạy, nó còn quan sát được quá trình của những dòng lệnh tuân thủ chạy, đánh giá cái dòng chảy data qua nó, và tối ưu hoá mã amys dựa trên những hiểu biết/ kiến thức đã có.
```

## What can in-browser JavaScript do?

JavaScript mới nhất là 1 ngôn ngữ code "an toàn" . nó không cung cấp quyền truy cập thấp vào bộ nhớ hoặc cpu, bởi vì nó được tạo ra với mục dích dành cho các browser mà không ccanf cái quyền truy cập đáy.

Khả năng cảu JavaScript phụ thuộc mạnh mẽ vào cái môi trường mà nó đang chạy. Đẻ ví dụ, tinh năng hỗ trợ của [Node.js](https://wikipedia.org/wiki/Node.js) cho phép JavaScript đọc và viết files bất kì, làm yêu cầu mạng, etc.

ở trong trình duyệt, JavaScript có thể làm bất cứ điều gì liên quan đến nhân bản Webpage, tương tác với người dùng, và webserver.

Để ví dụ, in-browser JavaScript có thể làm những điều sau:

- tạo thêm HTML cho trang, thay đổi những thứ đã có trước đó, và tạo kiểu.
- phản ứng lại với tương tác người dùng, chạy trên những cú click chuột, di chuyển con chỏ, bấm phím.
- gưit yêu cầu qua network đến những cái sever di động, download và upload files (còn đc gọi là [AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) và [COMET](https://en.wikipedia.org/wiki/Comet_(programming)) technologies).
- nhận và cài cookies, hỏi những người thăm quan trang web, Hiện tin nhắn
- Ghi nhớ data bên người dùng ("local storage").

## What CAN'T in-browser JavaScript do?

Khả năng của JavaScript được giới hạn lại để bảo vệ người dùng. Mục đích của việc này là để ngăn chặn những trang web xấu thâm nhập vào thông tin hoặc làm hại data riêng của người dùng.

Cí dụ của ngững giới hạn trên bao gồm:

- JavaScript trên trang web có thể không đọc và viết nhữ file không đồng bộ trên ổ cứng của thiết bị, sao chép hoặc thực hành trương trình. Nó không có truy cập trực tiếp vào chức năng của OS.

  Những trình duyệt tiên tiến cho phép nó truy cập/ làm việc với files, nhưng quyền truy cập bị hạn chế và chỉ cung cấp nếu người dùng làm những hành động chắc chắn/ xác thực, ví dụ như "dropping/ thả" một file vào của sổ trình duyệt hoặc chọn file thông qua 1 cái nhãn `<input>` .

  luôn có cách để tương tác với camera/microphone và những thiết bị khác, nhưng nó cần sự cho phép dõ dàng của nguồi dùng. Vậy nên những trang bật Javascript/JavaScript-enabled có thể không bật 1 cái web cam 1 cách lén lút, quan sát xung quanh và gửi thông tin về [NSA](https://en.wikipedia.org/wiki/National_Security_Agency).
- Những cái tabs/windows khác nhau đại khái là không biết nhau. Đôi khi có, Lấy ví dụ khi 1 Window dùng JavaScript để mở một cái Window khác. kể cả trong trường hợp này, JavaScript từ 1 trang web sẽ không truy cập vào trang web khác trừ khi cả 2 đến từ cùng 1 Site/ web (từ một lãnh thổ, biên bản hoặc cổng khác).

  Cái này được gọi là "Chính Sách nguồn gốc giống nhau/Same Origin Policy". Để làm việc quay quanh cái đấy, *Cả hai trang phải cho phép việc trao đổi data và phải chứa code JavaScript đặc biệt mà dùng để xử lý nó. Chúng ta sẽ học về nó trong hướng dẫn này.

  Một lần nữa, những cái giới hạn này là vì sự an taonf của người dùng. một trang từ `http://anysite.com` Nơi mà người dùng một khi đã mở thì sẽ không có quyền truy cập vào trang web khác với cái URL `http://gmail.com`, <- ví dụ, và trộm lấy thông tin từ đó.
- JavaScript có thể dễ dàng giao tiếp qua net đến cái sever làm ra từ trang bạn đang dùng. nhưng nó có khả năng nhận dữ liệu từ một site/lãnh địa khác mà bị què/hỏng/lỗi. Kể cả khi cso thể, nó yêu cầu sự sắp xếp dõ dàng (diễn đạt bằng tiêu đè HTTP ) từ 1 bên xa/ di động khác. một lần nữa, đó là giới hạn an toàn.

![](limitations.svg)

Sự giới hạn đó sẽ không tồn tại nếu JavaScript được dùng ngoài cái browser, lấy ví dụ trên 1 server. browsers tiên tiến cũng cho phép plugins/extensions cái mà có thể nới hạn quyền.

## What makes JavaScript unique?

Có ít nhất 3 điều tuyệt vời về JavaScript:

```compare
+ Hoà nhập hoàn toàn với HTML/CSS.
+ Những thứ đơn giản được làm dơn giản.
+ Được hỗ trợ bởi cái browser lớn và và được mặc định bật.
```

JavaScript là công nghệ về browser duy nhất mà có thể kết hợp lại 3 thứ trên.

Đó chính là thứ làm cho JavaScript đặc biệt. Đó là lý do tại sao đây lại là công cụ lớn rộng/ nổi tiếng nhất cho việc tạo ra giao diện của browser.

Điều đó nói rằng, JavaScript có thể dùng để tạo sever, ứng dụng di đỗng, etc.

## Languages "over" JavaScript

Cú pháp của JavaScript ko phù hợp với nhu cầu của tất cả mọi người. Mỗi 1 người một khác/ muốn 1 tính năng khác.

Điều đó được kỳ vọng, Bởi vì nhu cầu và dự án của mỗi người 1 khác/ khác nhau .

Cho nên, cho nên gần đây một số lượng lớn của các ngôn ngữ khác xuất hiện, which are *chuyển đổi* (converted) thành JavaScript trước khi đc chạy trên browser.

Những công cụ hiện đại làm cho sự chuyển dịch rất nhanh và minh bạch/ dõ dàng , cho phép các developers code ở ngôn ngữ khác và tự dộng chuyển đổi qua "trang thứ 3 /under the hood".

ví dụ của các ngôn ngữ đó:

- [CoffeeScript](https://coffeescript.org/) là "syntactic sugar/ miếng đường cú pháp" cho JavaScript. Nó cho bạn tiếp xúc với những cú pháp ngắn hơn, cho phép ta viết code rõ ràng và chuẩn xác hơn. Thường thì, Ruby devs like it.
- [TypeScript](https://www.typescriptlang.org/) tập trung vào việc công thêm "strict data typing/ gõ data nghiêm khắc" để đơn giản hoá phát triển và hỗ trợ những phần mềm phức tạp. được phát triển bởi Microsoft.
- [Flow](https://flow.org/) cũng là thêm gõ data, nhưng bằng cách khác. phát triển bởi Facebook.
- [Dart](https://www.dartlang.org/) là 1 ngôn ngữ đọc lập có engine của riêng nó và chạy trong môi trường không browser (như app điện thoại), những cũng cần phải được chuyển thể sang JavaScript. tạo ra bởi Google.
- [Brython](https://brython.info/) là bộ chuyển mã từ Python sang JavaScript, nó cho phép đọc và ứng dụng vào Python thuần tuý mà ko cần JavaScript.
- [Kotlin](https://kotlinlang.org/docs/reference/js-overview.html) nó là ngôn ngữ Programming tiên tiến, ngắn gọn và an toàn mà có thể chinh phục browser hoặc Node.

Còn nhiều cái khác nữa. Đương nhiên, kể cả nếu có dùng một trong những ngôn ngữ chuyển đổi nầy, chúng ta nên học JavaScript để có thể hoan toàn hiểu được những thứ ta dang làm.

## Summary

- JavaScript được tạo ra với mục đích là ngôn ngữ chỉ cho browser, nhưng bây giờ nó còn được dùng trong nhiều môi trường khác nữa.
- ngày nay, JavaScript có 1 chỗ đứng đặc biệt, được ví như là ngôn ngũ code browser được nhiều người đón nhận nhất, tích hợp hoàn toàn với HTML/CSS.
- Có trất nhiều ngôn ngữ đã bị "dịch mã" thành JavaScript và cung cấp những tính năng khác nhau. Những ngôn ngữ đấy được khuyên là dành thời gian va nghiên cứu chúng, và ít nhất, sau khi đã làm chủ được JavaScript.
