# Hello, world!

Trong phần này sẽ chỉ học về JavaScript, về ngôn ngũ này.

chúng ta cần một môi trường tốt để chạy script, bởi vì quyển sách này online, browser là 1 lựa chọn tốt.chúng tôi sẽ giữ những command browser cụ thể như (like `alert`) xuông mức tối thiểu để bạn không giành quá nhiều thời gian vào nó nêu bạn có dự định tập trung vào môi trường khác (like Node.js). We'll focus on JavaScript in the browser in the [next part](/ui) of the tutorial.

So first, let's see how we attach a script to a webpage. For server-side environments (like Node.js), you can execute the script with a command like `"node my.js"`.


## The "script" tag

JavaScript programs có thể chuyển thành tài liệu HTML ở hấu hết mọi nơi với việ dùng `<script>` tag.

For instance:

```html run height=100
<!DOCTYPE HTML>
<html>

<body>

  <p>Before the script...</p>

*!*
  <script>
    alert( 'Hello, world!' );
  </script>
*/!*

  <p>...After the script.</p>

</body>

</html>
```

```online
You can run the example by clicking the "Play" button in the right-top corner of the box above.
```

The `<script>` tag chứa JavaScript code sẽ tự động tiến hành khi browser chạy cái tag.


## Modern markup

The `<script>` tag có nhiều thuộc tính mà bây giờ hiếm khi được sử dụng nhưng vẫn đc tìm thấy ở code cũ:

The `type` thuộc tính: <code>&lt;script <u>type</u>=...&gt;</code>
: tiêu chuẩn HTML cũ, HTML4, yêu cầu script phải có `type`. thường thì là `type="text/javascript"`. bây giờ thì không cần nữa. Also, tiêu chuẩn HTML thời nay hoàn toàn thay đổi ý nghĩa của thuộc tính này. bây giờ nó có thể dung cho JavaScript modules. nhưng dố là chủ đề nâng cao, chúng ta sẽ nói về modules ở phần khác của tutorial.

thuộc tính của `language`: <code>&lt;script <u>language</u>=...&gt;</code>
: thuộc tính này dùng để chỉ ra ngôn ngữ của dong script. thuộc tính này không cồn ý nghĩa nừa vì JavaScript chính là ngôn ngữ default. không cần phải dùng nó.

Comments before and after scripts.
: ở rất nhiều quyển sách và hướng dẫn cũ, you may find comments inside `<script>` tags, like this:

    ```html no-beautify
    <script type="text/javascript"><!--
        ...
    //--></script>
    ```

    This trick không còn hoạt động ở JavaScript hiện đại. những lệnh này nhằm che giấu JavaScript code khỏi các browser cũ không biết cách chạy lệnh `<script>` tag. bời vì browser được phát hành trong 15 năm dổ lại đây không có lỗi này, dòng lệnh này có thể giúp bạn nhận biết được những code rất cũ


## External scripts

nếu ta có rất nhiều JavaScript code, ta có thể đặt nó vào những file riệng biệt
Script files được gắn vào HTML với thuộc tính `src`:

```html
<script src="/path/to/script.js"></script>
```

ở, `/path/to/script.js` nó là đường tuyệt đối đến script từ trang web góc. họ cũng có thể cung cấp một đường dẫn tương đối từ trang hiện tại. For instance, `src="script.js"`, cũng giống `src="./script.js"`, nghĩa là 1 `"script.js"` đang ở trong cái folder này.

ta cũng có thể đưa URL đầy đủ. For instance:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js"></script>
```

để găn nhiều script scripts, dùng nhiều tags:

```html
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
…
```

```smart
như quy luật, chỉ những script đơn giản nhất được dặt vào HTML. nhưng cái phức tạp hơn nằm trong các tệp riêng biệt.

lợi ích vủa các file riêng biệt là browser sẽ tự động tải về và dự trữ ở cache của nó [cache](https://en.wikipedia.org/wiki/Web_cache).

các trang khác mà có mối quan hệ với the same script sẽ lấy script từ cache mà không cần phải download nó, nên cái file chỉ cần được download 1 lần.

giúp giảm tải lưu lượng dữ liệu và làm trang web nhanh hơn.
```

````warn header="If `src` is set, the script content is ignored."
A single `<script>` tag can't have both the `src` attribute and code inside.
một khi đã đạt 'SCR' thì dòng script sẽ bị bỏ qua
một script không thể có cả thuộc tính SCR và mã ở bên trong
This won't work:

```html
<script *!*src*/!*="file.js">
  alert(1); // the content is ignored, because src is set
</script>
```

chúng ta phải chọn giữa `<script src="…">` bên ngoài hoặc là `<script>` đươn giản với code.

The example above can be split into two scripts to work:

```html
<script src="file.js"></script>
<script>
  alert(1);
</script>
```
````

## Tổng kết

- dùng lệnh `<script>` để thêm JavaScript code vào 1 trang.
- thuộc tính `type` và `language`là không cần thiết/ yêu cầu.
- Script ở trong một file bên ngoài có thể thêm vào dùng lệnh `<script src="path/to/script.js"></script>`.


There is much more to learn about browser scripts and their interaction with the webpage. But let's keep in mind that this part of the tutorial is devoted to the JavaScript language, so we shouldn't distract ourselves with browser-specific implementations of it. We'll be using the browser as a way to run JavaScript, which is very convenient for online reading, but only one of many.
