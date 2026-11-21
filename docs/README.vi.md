# SilverZAgents — Tiếng Việt

Ứng dụng Windows hỗ trợ cấu hình và theo dõi các tác vụ Facebook trên những hồ sơ trình duyệt bạn đã đăng nhập.

**Đây là kho phân phối chính thức, không phải kho source mở.** Tải bộ cài `.exe` tại [Releases](https://github.com/silverznet/SilverZAgents/releases/tag/v6.0.0-preview.1). Các tệp “Source code” do GitHub tự tạo chỉ chứa tài liệu công khai của kho này.

## Big Update · 6.0.0 Preview 1

Thêm quản lý Trang/Profile: chạy riêng hoặc sau mỗi vòng tương tác thành công; gán đúng nơi quản lý theo từng kết nối hồ sơ; chọn chỉ kiểm tra, lưu nháp hoặc tự trả lời. Tin nhắn mặc định tắt. FAQ đã duyệt dùng chung giúp giảm gọi AI, còn hội thoại và cache phản hồi được tách theo nơi quản lý.

Sau cập nhật, tải lại extension **3.1.0** trong từng hồ sơ. Vào **Nhiệm vụ → Tương tác & Quản lý Trang/Profile** để gán nơi quản lý và cấu hình. Nên bắt đầu bằng soạn nháp. Giao diện hộp thư chưa xác minh được sẽ báo cần kiểm tra, không tự gửi. Xem [Hướng dẫn quản lý](MANAGEMENT.md).

## Chức năng

- Like, Like/Tim xen kẽ hoặc chọn cảm xúc ngẫu nhiên; bình luận bằng nội dung dựng sẵn hoặc AI theo ngữ cảnh.
- Đăng chữ, ảnh, nhiều ảnh, chữ + ảnh, URL và Share vào danh sách nhóm; số bài mỗi nhóm tùy chỉnh.
- Đa hồ sơ/đa trình duyệt Chrome, Edge, Brave, Cốc Cốc; theo dõi từng job và điều kiện dừng riêng.
- Chạy một lần/lặp, theo phút/số bài, nghỉ định kỳ rồi tiếp tục, tổng điều kiện dừng, phạm vi Nhóm hoặc Trang chủ độc lập và F5.
- Bộ não Online với các API được người dùng cấu hình; Offline với model local tải riêng. Nội dung dựng sẵn và đăng chỉ ảnh không cần AI tạo nội dung.
- Nhật ký, bộ nhớ, ngôn ngữ Việt/Anh, sáng/tối, thông báo cuối phiên và ghi nhớ cửa sổ.

## Cài đặt

1. Tải `SilverZAgents-6.0.0-preview.1-Setup.exe` và `SHA256SUMS.txt`, kiểm tra mã SHA-256.
2. Chạy bộ cài, chọn thư mục riêng như `D:\Program Files\SilverZAgentsClient`. Cần Internet nếu thiếu runtime hoặc thư viện.
3. Bộ cài dùng lại Python 3.14 x64 tương thích. Nếu chỉ có Python 3.15/nhánh khác, bộ cài giữ nguyên và có thể cài runtime riêng sau khi bạn chấp nhận giấy phép Python.
4. Cài extension từ cùng một thư mục `extension` vào từng hồ sơ muốn dùng, kiểm tra bản **3.1.0**.
5. Mở tab Facebook bằng tài khoản của bạn, đặt tác vụ nhỏ rồi chủ động bấm bắt đầu.

Xem [hướng dẫn chi tiết và cài bằng CMD](INSTALL.md). Bấm X chỉ thu nhỏ xuống taskbar; thoát hẳn tại **Cài đặt → Thoát hoàn toàn**.

## Trạng thái & dữ liệu

Bản **6.0.0 Preview 1** đang được hoàn thiện. Đã kiểm thử tự động/mô phỏng; chưa nghiệm thu mọi PC khách và mọi giao diện Facebook thực tế. Không bảo đảm bình luận đã xuất hiện chỉ vì đã gửi Enter, cũng không bảo đảm bài được quản trị nhóm phê duyệt.

Online gửi phần ngữ cảnh cần thiết tới API bạn chọn và có thể phát sinh phí theo nhà cung cấp. Offline suy luận tại máy sau khi tải model; Facebook vẫn cần mạng. Không kèm tài khoản hay API key. Hồ sơ và đăng nhập thuộc trình duyệt của người dùng. Chia sẻ thống kê kiến thức là tùy chọn, mặc định tắt; không có dịch vụ máy chủ đi kèm bản này.

Source master không được công bố. Lõi Python đã biên dịch, một số tài nguyên đã mã hóa; extension vẫn có thể được xem. Không có biện pháp chống dịch ngược tuyệt đối. Chữ ký kiểm tra gói không phải chứng thư Windows Authenticode.

Chưa có tự cập nhật client hoặc kích hoạt bản quyền thương mại. Tải và cài bản cập nhật thủ công từ Releases. Chỉ thao tác trên tài khoản/nội dung bạn có quyền quản lý, tôn trọng nội quy nhóm và điều khoản nền tảng.

© 2026 SilverZ.Net · Lập trình bởi Phạm Hồng Quang  
Liên hệ: **hello@silverz.net** · https://silverz.net
