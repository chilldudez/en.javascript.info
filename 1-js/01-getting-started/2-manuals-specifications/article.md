# Manuals and specifications

Quyển sách này là hướng dẫn. Với mục đích dần dần giúp bạn học được ngôn ngũ. Nhưng 1 khi đã làm quen được với ngôn ngữ này thì bạn sẽ cần các nguồn khác.

## Specification

[The ECMA-262 specification](https://www.ecma-international.org/publications/standards/Ecma-262.htm) chứa thông tin chính thức sâu, và chi tiết nhất về JavaScript. NÓ định hình ngôn ngữ.

Bởi vì nó theo hình thức như thế, cho nên ban đầu nó rất khó để hiểu. nên nếu bạn cần 1 nguồn thông tin đấng tin tưởng về chi tiết của ngôn ngữ, the specification là nơi bạn có thể tin tưởng. nhưng nó không phải lựa chọn hằng ngày .

mỗi năm sẽ có 1 phiên bản phân loại mới. giữa các bản ra mắt, bản phân loại nháp mới nhất là [https://tc39.es/ecma262/](https://tc39.es/ecma262/).

để đọc về các tính năng tối tân mới, bao gồm cả "cận kề tiêu chuẩn" (còn được gọi là "stage 3"), xem đề xuất tại [https://github.com/tc39/proposals](https://github.com/tc39/proposals).

Và nếu bạn đang DEV một cái browser, thì sẽ có các phân loại khác đc ghi ở [second part](info:browser-environment) của hướng dẫn.

## Manuals

- **MDN (Mozilla) JavaScript Reference** là hướng dẫn chính với ví dụ và thông tin. nó rất tốt để tìm kiếm thông tin xâu về cơ chế ngôn ngữ riêng biệt, cách/methods etc.

  You can find it at [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference).

mặc dù, nó thường được dùng cho các cái tìm kiếm quan trọng trên internet. Chỉ cần dùng "MDN [term]" ở trong query, e.g. [https://google.com/search?q=MDN+parseInt](https://google.com/search?q=MDN+parseInt) để tìm kiếm chức năng `parseInt`.

## Compatibility tables

JavaScript là ngôn ngữ để dev, những tính năng mới được thêm vào liên tục.

To see their support among browser-based and other engines, see:

- [https://caniuse.com](https://caniuse.com) - per-feature tables of support, e.g. to see which engines support modern cryptography functions: [https://caniuse.com/#feat=cryptography](https://caniuse.com/#feat=cryptography).
- [https://kangax.github.io/compat-table](https://kangax.github.io/compat-table) - a table with language features and engines that support those or don't support.

tất cả những nguồn tài liệu này để hữu ích cho việc phát triển sau này, vì nó chứa đựng rất nhiều thông tin hữu ích về chi tiết của ngôn ngữ, their support, etc.

hãy ghi nhớ những trang này (or this page) trong trường hợp bạn cần thông tin sâu xắc về một chức năng (đặc biệt) nào đó.
