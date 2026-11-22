# CASERY — Website Prototype V1

Dark gaming storefront / event hub lấy cảm hứng từ cách tổ chức điều hướng Discord, sử dụng nhận diện CASERY riêng. Đây là **prototype HTML/CSS/JS** có thể chạy trên GitHub Pages không cần cài đặt thư viện hay backend.

## Xem ngay

Mở `index.html` bằng Chrome, Edge hoặc Safari. Không cần chạy server. Font sẽ sử dụng DM Sans/Space Grotesk nếu có Internet, và tự dùng font dự phòng nếu không có.

## Tính năng đã có trên bản demo

- Giao diện dark gaming, responsive desktop/mobile.
- Thanh menu trái có thể thu gọn bằng nút ☰; các mục Kho cá nhân, Cộng đồng và Tìm hiểu thêm có thể mở/đóng.
- Spotlight `Is My Partner a Spy?` và game mùa `Ashford: A Winter Mystery`.
- Bộ lọc game (demo / sự kiện / sắp ra mắt) và tìm kiếm (`⌘ K` / `Ctrl K`).
- Cửa sổ chi tiết game, wishlist lưu bằng localStorage trên trình duyệt.
- Countdown minh họa sự kiện Christmas 05–31/12/2026 theo múi giờ +07:00.
- Leaderboard **dữ liệu mẫu**, đồng hồ speedrun thử trên trình duyệt và lưu kết quả local (không phải leaderboard online).
- Khu bình luận công khai **dữ liệu mẫu**, khu Aftercase Room **mô phỏng ý tưởng premium**.
- Hộp thoại giải thích quy tắc event, cách chơi và tính điểm.

## Chưa có (cần backend trước khi kinh doanh thật)

1. Tạo tài khoản, xác thực, quản lý profile, quản lý game đã mua.
2. Upload game / hosting web build / game download / quyền phân phối và bản quyền.
3. Thanh toán thật, hóa đơn, hoàn tiền; áp dụng điều khoản game chỉ bán trong thời gian diễn ra sự kiện.
4. Matchmaking, phòng chơi và đồng bộ phiên chơi co-op.
5. Server-side game timer, xác thực kết quả, anti-cheat, đồng bộ bảng xếp hạng, phát thưởng.
6. Hệ thống bình luận và moderation thật; phân quyền spoiler premium, tôn trọng privacy và quyền truy cập.

**Lưu ý:** Game demo chưa được nhúng và các giá trị như sản phẩm sắp phát hành, mùa giải, reward, review, bảng xếp hạng hiện là **placeholder để review thiết kế**. Không giả định đã có giao dịch hay dữ liệu người chơi.

## Đưa lên GitHub Pages (không cần terminal)

1. Tạo repository mới trên GitHub, gợi ý tên `casery-games` và chọn **Public** nếu muốn website public với GitHub Pages thông thường.
2. Chọn **Add file → Upload files**, kéo thả `index.html` và `README.md` (không upload nguyên file zip vì GitHub không tự bung zip).
3. Chọn **Commit changes**.
4. Vào **Settings → Pages**.
5. Trong **Build and deployment**, chọn **Deploy from a branch** → Branch `main` → Folder `/(root)` → **Save**.
6. Mở URL GitHub Pages được GitHub hiển thị trong phần Pages sau khi triển khai xong.

Website không sử dụng đường dẫn tuyệt đối nên có thể hoạt động với repo Pages dạng `/casery-games/`.

## Sửa nội dung

- Phần danh sách game: tìm `const GAMES=[` trong `index.html`.
- Thông tin sự kiện: tìm `05.12` hoặc `updateEvent()`; đây là ngày **minh họa**.
- Màu giao diện: tìm `:root{` ở đầu CSS, đổi `--accent`, `--bg`, `--side`.
- Tiêu đề spotlight: tìm `LOVE IS A` trong hero.
- Dữ liệu bảng xếp hạng minh họa: tìm `demoScores`.
- Các tính năng thật cần có backend (ví dụ Supabase/Firebase + server/API), không thể làm an toàn chỉ với HTML tĩnh.

## Lựa chọn tiếp theo

Khi nhóm có trang tham chiếu khác, chỉnh lại sidebar, game cards, gamification và tone màu dựa trên feedback. Bản này là V1 cho việc duyệt định hướng visual và cấu trúc tính năng.
