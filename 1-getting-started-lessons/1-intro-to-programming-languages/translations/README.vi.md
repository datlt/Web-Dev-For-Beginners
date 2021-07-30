# Giới thiệu về ngôn ngữ lập trình và công cụ liên quan

Bài học này bao gồm những kiến thức cơ bản về ngôn ngữ lập trình. Các chủ đề được đề cập ở đây áp dụng cho hầu hết các ngôn ngữ lập trình hiện đại ngày nay. Trong phần 'Công cụ', bạn sẽ tìm hiểu về phần mềm hữu ích cho bọn trong vai trò là nhà phát triển(developer).

![Intro Programming](/sketchnotes/webdev101-programming.png)
> Sketchnote by [Tomomi Imura](https://twitter.com/girlie_mac)

## Trắc nghiệm trước khi bắt đầu
[Pre-lecture quiz](https://nice-beach-0fe9e9d0f.azurestaticapps.net/quiz/1)

## Giới thiệu

Bài học này sẽ đề cập đến những nội dung dưới đây:

- Lập trình là gì?
- Các loại ngôn ngữ lập trình
- Các yếu tố cơ bản của một chương trình
- Phần mềm và công cụ hữu ích cho nhà phát triển chuyên nghiệp

## Lập trình là gì?

Lập trình (còn được gọi là viết code) là quá trình viết các chỉ lệnh cho một thiết bị, chẳng hạn như máy tính hoặc thiết bị di động. Các chỉ lệnh này được viết bằng ngôn ngữ lập trình, ngôn ngữ này sau đó sẽ được thiết bị thông dịch. Những bộ chỉ lệnh này có thể được gọi bằng nhiều tên khác nhau, trong đó *program(chương trình)*, *computer program(chương trình máy tính)*, *application(ứng dụng) (app)* và *executable(thực thi)* là một số tên phổ biến.

Một *program(chương trình)* có thể là bất kỳ thứ gì được viết bằng code; ví dụ như trang web, trò chơi hoặc ứng dụng điện thoại. Mặc dù có thể tạo một chương trình mà không cần viết code, nhưng logic ẩn phía dưới sẽ được thông dịch cho thiết bị và logic đó thông thường sẽ phải viết bằng code. Một chương trình đang *đang chạy(running)* hoặc *đang thực thi code(executing code)* có nghĩa là đang thiết bị của bạn đang thực hiện các chỉ lệnh mà nó nhận được trong chương trình. Thiết bị mà bạn đang dùng để đọc bài viết này cũng đang thực hiện một chương trình để hiển thị bài viết lên màn hình.

✅ Hãy làm một nghiên cứu nhỏ: người được coi là lập trình viên máy tính đầu tiên trên thế giới?

## Ngôn ngữ lập trình

Ngôn ngữ lập trình phục vụ một mục đích chính: để các nhà phát triển xây dựng các chỉ lệnh để gửi đến một thiết bị. Các thiết bị chỉ có thể hiểu được ngôn ngữ dưới dạng nhị phân (1 và 0), đối với *hầu hết* các nhà phát triển thì đó không phải là cách giao tiếp hiệu quả. Ngôn ngữ lập trình là phương tiện giao tiếp giữa con người và máy tính.

Ngôn ngữ lập trình khác nhau có định dạng khác nhau và có thể phục vụ các mục đích khác nhau. Ví dụ: JavaScript chủ yếu được sử dụng để tạo ứng dụng web, trong khi Bash chủ yếu được sử dụng trong các hệ điều hành.

Đối với máy tính, *Ngôn ngữ cấp thấp* thường dễ hiểu hơn so với *ngôn ngữ cấp cao*. Tuy nhiên, ngôn ngữ cấp cao lại được sử dụng phổ biến vì nó dễ đọc hơn đối với con người (chính là người viết code). JavaScript được coi là một ngôn ngữ cấp cao.

Đoạn mã sau minh họa sự khác biệt giữa ngôn ngữ cấp cao với JavaScript và ngôn ngữ cấp thấp với mã hợp ngữ ARM.

```javascript
let number = 10
let n1 = 0, n2 = 1, nextTerm;

for (let i = 1; i <= number; i++) {
    console.log(n1);
    nextTerm = n1 + n2;
    n1 = n2;
    n2 = nextTerm;
}
```

```c
 area ascen,code,readonly
 entry
 code32
 adr r0,thumb+1
 bx r0
 code16
thumb
 mov r0,#00
 sub r0,r0,#01
 mov r1,#01
 mov r4,#10
 ldr r2,=0x40000000
back add r0,r1
 str r0,[r2]
 add r2,#04
 mov r3,r0
 mov r0,r1
 mov r1,r3
 sub r4,#01
 cmp r4,#00
 bne back
 end
```

Tin hay không tùy bạn, *hai  chương trình này đang thực hiện cùng một việc*: in một dãy Fibonacci lên đến 10.

✅ Dãy Fibonacci là dãy số bắt đầu bằng 0,1 trong đó số tiếp theo là tổng của 2 số liền trước nó.

## Thành phần của một chương trình

Một lệnh đơn nhất trong chương trình được gọi là *câu lệnh* và thường sẽ có ký tự hoặc khoảng cách dòng đánh dấu nơi lệnh kết thúc. Cú pháp để kết thúc chương trình thay đổi tuỳ theo từng ngôn ngữ.

Hầu hết các chương trình nhận dữ liệu từ người dùng hoặc từ thiết bị khác để hoạt động. Chương trình có thể thay đổi cách xử lý tuỳ thuộc vào dữ liệu. Các ngôn ngữ lập trình có một cách để lưu trữ tạm thời dữ liệu để tiện truy cập. Dữ liệu này được gọi là *biến*. Biến là các câu lệnh chỉ dẫn một thiết bị lưu dữ liệu trong bộ nhớ của nó. Các biến trong chương trình tương tự như các biến trong đại số, nơi chúng có một tên duy nhất và giá trị của chúng có thể thay đổi theo thời gian.

Một số câu lệnh có thể sẽ không được thiết bị thực thi. Điều này thường là do chủ ý thiết kế bởi nhà phát triển hoặc do chương trình xảy ra lỗi không mong muốn. Tùy từng điều kiện, chương trình có thể thực hiện các chỉ lệnh khác nhau. Một câu lệnh phổ biến trong các ngôn ngữ lập trình hiện đại để kiểm soát cách một chương trình được chạy là câu lệnh `if..else`.

✅ Bạn sẽ được học thêm về loại câu lệnh này trong các bài học tiếp theo 

## Các công cụ hữu ích

[![Tools of the Trade](https://img.youtube.com/vi/69WJeXGBdxg/0.jpg)](https://youtube.com/watch?v=69WJeXGBdxg "Tools of the Trade")

> 🎥 Click the image above for a video about tooling

Trong phần này, bạn sẽ học về một số phần mềm mà bạn có thể thấy rất hữu ích trong hành trình trở thành developer

**Môi trường phát triển** là một tập hợp các công cụ và tính năng mà một developer thường sử dụng khi viết phần mềm. Một số công cụ được tùy chỉnh cho nhu cầu cụ thể của developer và có thể thay đổi theo thời gian nếu developer thay đổi mức độ ưu tiên trong công việc, hoặc dự án cá nhân, hoặc khi họ chuyển sang sử dụng một ngôn ngữ lập trình khác. Môi trường phát triển cũng thể hiện tính cách như các developer sử dụng chúng. 

### Trình soạn thảo - Editors

Một trong những công cụ quan trọng nhất để phát triển phần mềm là trình soạn thảo. Editors là nơi bạn viết code và đôi khi là nơi bạn sẽ chạy code mà mình đã viết. 

Ngoài ra có một vài lý do khác mà developer sử dụng Editors:

- *Debugging Gỡ lỗi* Phát hiện lỗi bằng cách xem từng đoạn code, từng dòng một. Một số editors có khả năng gỡ lỗi hoặc có thể được tùy chỉnh và thêm chức năng với các ngôn ngữ lập trình cụ thể. 
- *Syntax highlighting - đánh dấu cú pháp* Thêm màu sắc và định dạng văn bản vào code, giúp code đọc hơn. Hầu hết các editors đều cho phép tùy chỉnh định dạng code. 
- *Extensions and Integrations* Additions that are specialized for developers, by developers, for access to additional tools that aren't built into the base editor. For example, many developers also need a way to document their code and explain how it works and will install a spell check extension to check for typos. Most of these additions are intended for use within a specific editor, and most editors come with a way to search for available extensions.
- *Tiện ích mở rộng và tích hợp* Các bổ sung dành riêng cho developer, bởi các developer, để truy cập vào các tools bổ sung không có sẵn trong trình soạn thảo ban đầu. Ví dụ: nhiều developer cũng cần viết tài liệu giải thích cho code đã viết, khi đó họ có thể sẽ đặt tiện ích mở rộng để kiểm tra lỗi chính tả.
- *Tùy biến* Hầu hết editors đều có khả năng tùy biến rất cao, mỗi developer có thể tùy biến môi trường phát triển của mình tùy theo nhu cầu một cách không đụng hàng với ai. Rất nhiều developer còn tự code lấy cho mình những phần mở rộng riêng

#### Editors và Phần mở rộng phổ biến cho Web Development (Phát triển web)

- [Visual Studio Code](https://code.visualstudio.com/)
  - [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
  - [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack)
  - [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Atom](https://atom.io/)
  - [spell-check](https://atom.io/packages/spell-check)
  - [teletype](https://atom.io/packages/teletype)
  - [atom-beautify](https://atom.io/packages/atom-beautify)

### Trình duyệt - Browsers

Một công cụ quan trọng khác là trình duyệt. Web developers dùng trình duyệt để xem kết quả khi code của họ chạy trên web, nó cũng được dùng để hiển thị một cách trực quan các thành phần của một trang web được viết trong editors, ví dụ như HTML.

Nhiều trình duyệt còn tích hợp sẵn *công cụ phát triển* (DevTools) 
Many browsers come with *developer tools* (DevTools) chứa một tập hợp các tính năng và thông tin hữu ích để hỗ trợ developer thu thập và nắm bắt thông tin về ứng dụng của họ. Ví dụ: Nếu một trang web có lỗi, sẽ rất hữu ích nếu bạn biết điều kiện và tình huống nó xảy ra. DevTools trong trình duyệt có thể được sử dụng để nắm bắt thông tin này. 

#### Trình duyệt và DevTools phổ biến

- [Edge](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium?WT.mc_id=academic-13441-cxa)
- [Chrome](https://developers.google.com/web/tools/chrome-devtools/)
- [Firefox](https://developer.mozilla.org/docs/Tools)

### Công cụ dòng lệnh 

Một số dev đơn giản thích chế độ dòng lệnh hơn. Việc viết code đòi hỏi phải gõ phím khá nhiều và một số dev thích sử dụng phím tắt thay vì chuột để di chuyển qua lại giữa các màn hình, mở các files khác nhau hay chạy các tools liên quan. Hầu hết các tác vụ có thể được hoàn thành bằng chuột, nhưng một lợi ích của việc sử dụng dòng lệnh là có thể thực hiện nhiều việc mà không cần phải hoán đổi giữa chuột và bàn phím. Môi trường phát triển được tùy chỉnh theo nhu cầu, sở thích của mỗi dev, có người sẽ tránh sử dụng dòng lệnh, một số sẽ sử dụng dòng lệnh hoàn toàn và một số thích kết hợp cả hai. 

### Tùy chọn dòng lệnh phổ biến

Tùy chọn sẽ thay đổi tùy theo hệ điều hành mà bạn sử dụng

*💻 = đã được tích hợp sẵn vào hệ điều hành*

#### Windows

- [Powershell](https://docs.microsoft.com/powershell/scripting/overview?view=powershell-7?WT.mc_id=academic-13441-cxa) 💻
- [Command Line](https://docs.microsoft.com/windows-server/administration/windows-commands/windows-commands?WT.mc_id=academic-13441-cxa) (also known as CMD) 💻
- [Windows Terminal](https://docs.microsoft.com/windows/terminal/?WT.mc_id=academic-13441-cxa)
- [mintty](https://mintty.github.io/)
  
#### MacOS

- [Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac) 💻
- [iTerm](https://iterm2.com/)
- [Powershell](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-7?WT.mc_id=academic-13441-cxa)

#### Linux

- [Bash](https://www.gnu.org/software/bash/manual/html_node/index.html) 💻
- [KDE Konsole](https://docs.kde.org/trunk5/en/konsole/konsole/index.html)
- [Powershell](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7?WT.mc_id=academic-13441-cxa)

#### Công cụ dòng lệnh phổ biến

- [Git](https://git-scm.com/) (💻 on most operating sytems)
- [NPM](https://www.npmjs.com/)
- [Yarn](https://classic.yarnpkg.com/en/docs/cli/)

### Tài liệu

Khi dev muốn học cái gì mới, họ thường sẽ đọc tài liệu về nó. Dev thường xuyên sử dụng tài liệu để tìm hướng dẫn về cách sử dụng tools và ngôn ngữ lập trình, và cũng để hiểu rõ hơn về cách nó hoạt động

#### Tài liệu Phổ biến về Phát triển Web 

- [Mozilla Developer Network (MDN)](https://developer.mozilla.org/docs/Web), from Mozilla, the publishers of the [Firefox](https://www.mozilla.org/firefox/) browser
- [Frontend Masters](https://frontendmasters.com/learn/)
- [Web.dev](https://web.dev), from Google, publishers of [Chrome](https://www.google.com/chrome/)
- [Microsoft's own developer docs](https://docs.microsoft.com/microsoft-edge/#microsoft-edge-for-developers), for [Microsoft Edge](https://www.microsoft.com/edge)

✅ Bây giờ bạn đã biết những điều cơ bản về môi trường của nhà phát triển web, hãy so sánh và đối chiếu nó với môi trường của nhà thiết kế web. 

---

## 🚀 Challenge
So sánh một số ngôn ngữ lập trình. Một số đặc điểm khác biệt của JavaScript so với Java là gì? Tương tự COBOL so với Go? 

## Post-Lecture Quiz
[Post-lecture quiz](https://nice-beach-0fe9e9d0f.azurestaticapps.net/quiz/2)

## Review & Tự học

Nghiên cứu một chút về các ngôn ngữ khác nhau có sẵn cho lập trình viên. Cố gắng viết một dòng bằng một ngôn ngữ, sau đó viết lại bằng một ngôn ngữ khác. Cảm nhận xem bạn đã học được gì? 

## Bài tập

[Đọc tài liệu](assignment.vi.md)
