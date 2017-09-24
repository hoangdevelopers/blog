---
title: Series JS để gió cuốn đi - JSDoc là gì? (Phần 1)
date: 2017-09-25 00:56:26
categories:
- JavaScript
tags:
- JSDoc3
- JSDoc
- JavaScript
clearReading: true
thumbnailImage: thumbnail.png
thumbnailImagePosition: right
autoThumbnailImage: yes
---
{% asset_img thumbnail.png %}
{% blockquote %}
    JSDoc là một ngôn ngữ đánh dấu dùng để chú thích tập tin mã nguồn JavaScript. Sử dụng chú thích JSDoc, lập trình viên có thể thêm tài liệu mô tả các application programming interface cho code của họ đang viết ra. Sau đó được xử lý, bởi các công cụ khác nhau, để tạo ra các tài liệu trong các định dạng tiếp cận như HTML và Rich Text Format.
    @wikipedia:en.wikipedia.org/wiki/JSDoc
{% endblockquote %}
Tại sao cần JSDoc?

Với JSDoc bạn chỉ cần thêm 1 plugin để generate tài liệu ra 1 trang web. Vậy là bạn đã có 1 trang Document cho code của mình rồi ^^!.
Minh họa 1 chút nha:
{% youtube vIclAOi3Hc0 640 360 %}
à mình đùa chút thôi thực ra thì… Sống trên đời...
{% asset_img songtren1dongtien.jpg %}
Thêm chú thích cho JavaScript

Thông thường JSDoc comment nên được đặt ở phía trước code của bạn. Nó phải bắt đầu bằng chuỗi /*** để được định dạng như 1 cú pháp JSDoc. Phần chú thích bắt dầu bằng /*, /*** hoặc nhiều hơn 3 dấu * sẽ bị bỏ qua.

Một đoạn chú thích đơn giản sẽ trông như dưới đây:

{% codeblock %}
/** This is a description of the foo function. */
function foo() {
}
{% endcodeblock %}
Bạn có thể gửi thêm thông tin như tác giả, mô tả..vv bằng các thẻ đặc biệt.
Trong ví dụ dưới dây, nếu function là một hàm khởi tạo (constructor).

Sử dụng thẻ mô tả code:

{% codeblock %}
/**
 * Represents a book.
 * @constructor
 */
function Book(title, author) {
}
{% endcodeblock %}
Có nhiều thẻ để bạn thể hiện thêm các thông tin khác nhau. Đọc bài Series JSDoc3 - Danh sách các thẻ được sử dụng trong JSDoc3 (phần 2) để tìm hiểu.

Ví dụ bổ xung thêm thông tin với các thẻ:

{% codeblock %}
/**
 * Represents a book.
 * @constructor
 * @param {string} title - The title of the book.
 * @param {string} author - The author of the book.
 */
function Book(title, author) {
}
{% endcodeblock %}
Generate tài liệu

Bạn có thể sử dụng công cụ JSDoc3 Tool để tạo ta trang web HTML chứa tài liệu comment,
Mặc định JSDoc sẽ sử dụng template default để trả về trong code HTML, bạn có thể edit hoặc tạo mới template nếu cần.
Chạy dòng lệnh cmd để generate tài liệu:

./jsdoc book.js

Nguồn:: http://usejsdoc.org/about-getting-started.html