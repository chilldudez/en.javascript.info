# Code editors

A code editor là nơi lập trình viên rành nhiều thời gian.

có 2 loại code editors chính: IDEs và lightweight editors. Rất nhiều người dùng 1 công cụ từ mỗi loại.

## IDE

The term [IDE](https://en.wikipedia.org/wiki/Integrated_development_environment) (Integrated Development Environment) được coi là 1 cái editor rất mạnh với rất nhiều tính năng thường để chạy trên một "project đầy dủ." như đã đc đề xuất , nó không chỉ là một editor, nhưng là "development environment/môi trường dev" toàn diện

IDE loads/tải toàn bộ dự án (có thể chứa rất nhiều files), cho phép điều hướng giữa các files, cho phép tự động hoằn thành dựa trên toàn bộ dự án (không chỉ những file đã mở), và thích hợp với phiên bản quản lý hệ thống (like [git](https://git-scm.com/)), một nơi để thử nghệm, và còn những "project-level" nữa.

nếu bạn chưa muốn lựa chọn IDE , hãy tham khảo các cái này:

- [Visual Studio Code](https://code.visualstudio.com/) (cross-platform, free).
- [WebStorm](https://www.jetbrains.com/webstorm/) (cross-platform, paid).

trên Window, còn có "Visual Studio", nhưng nó không phải là "Visual Studio Code". "Visual Studio" nó là một cái editor mạnh chỉ dành cho WIn, rất phù hợp cho nền tảng .NET . nó cũng tốt với JavaScript. và nó free [Visual Studio Community](https://www.visualstudio.com/vs/community/).

Rất nhiều IDEs phải mất phí, những họ sẽ cho bạn miễn phí thử nhiệm 1 thời gian. Phí cảu những cái web đấy không đáng kể so với đồng lương của các dev tiêu chuẩn, nên hãy chọn 1 cái cho bạn.

## Lightweight editors

"Lightweight editors/ editor nhẹ" không mạnh bằng IDEs, đổi lại thì nó nhanh, đơn giản/lịch sự và dễ hiểu.

được dùng chủ yếu để mở hoặc edit một files ngay tức thì.

điểm khác biệt chinhsn giữa "lightweight editor" và "IDE" là IDE làm việc trên project-level/ level dự án, nên phải load nhiều data hơn khi bắt đàu, phân tích cấu trúc dự án nếu cần và nhiều hơn thế. lightweight editor nhanh hơn nếu chỉ cần làm việc với file.

trông luyện tập, lightweight editors có thể có rất nhiều bổ sung trong đó bao gồm cú pháp phân tích level từ điển và autocompleters/ máy tự động hoàn thành, nên sẽ không có biên giới ngiêm ngặt nào giữa lightweight editor và IDE.

có rất nhiều lựa chọn, for instance:

- [Sublime Text](https://www.sublimetext.com/) (cross-platform, shareware).
- [Notepad++](https://notepad-plus-plus.org/) (Windows, free).
- [Vim](https://www.vim.org/) và [Emacs](https://www.gnu.org/software/emacs/) are also cool if you know how to use them.

## Let's not argue

những cái editors trên là những thứ tôi và bạn của tôi, những người tôi cho rằng là dev giỏi đang và đã dùng và cảm thấy hài lòng khi sử dụng nó.

Còn rất nhiều editors khác ở thế giới bên ngoài kia. hyax chọn cái mà bạn thích nhất.

lựa chọn của một editor, như những công cụ khác, nó cá nhân và phụ thuộc vào dự án, thói quen của bạn, và sở thích cá nhân.

The author's personal opinion:

- I'd use [Visual Studio Code](https://code.visualstudio.com/) if I develop mostly frontend.
- Otherwise, if it's mostly another language/platform and partially frontend, then consider other editors, such as XCode (Mac), Visual Studio (Windows) or Jetbrains family (Webstorm, PHPStorm, RubyMine etc, depending on the language).
