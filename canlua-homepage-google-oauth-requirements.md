# Yêu cầu viết lại trang index cho Privacy Policy Hub / CanLua

## 1. Mục tiêu

Viết lại file `index.html` của website:

`https://nhthien68.github.io/privacy-policy/`

Trang này vừa là **homepage công khai của ứng dụng CanLua** dùng trong
Google OAuth Branding Verification, vừa có thể giữ vai trò trang tổng
hợp Privacy Policy cho các ứng dụng khác.

Ưu tiên cao nhất là giúp Google xác định rõ:

-   Tên ứng dụng là **CanLua**.
-   CanLua là một ứng dụng thật, có mục đích/chức năng được mô tả rõ
    ràng.
-   Trang có thể truy cập công khai, **không yêu cầu đăng nhập**.
-   Trang có liên kết dễ thấy tới Privacy Policy của CanLua.
-   Trang giải thích minh bạch lý do CanLua sử dụng Google Sign-In và dữ
    liệu Google được yêu cầu.
-   Tên **CanLua** trên homepage phải khớp chính xác với App name trên
    Google OAuth consent screen.

Google OAuth hiện cấu hình:

-   **App name:** `CanLua`
-   **Application home page:**
    `https://nhthien68.github.io/privacy-policy/`
-   **Application privacy policy:**
    `https://nhthien68.github.io/privacy-policy/app-can-lua/`
-   **Authorized domain:** `nhthien68.github.io`

Website/property đã được xác minh quyền sở hữu bằng Google Search
Console cho URL prefix:

`https://nhthien68.github.io/privacy-policy/`

------------------------------------------------------------------------

## 2. Lý do cần sửa

Google OAuth Branding Verification trước đây báo các lỗi liên quan đến
homepage:

1.  Homepage chưa được xác minh quyền sở hữu.
2.  Homepage bị đánh giá như nằm sau login hoặc không cung cấp đủ thông
    tin công khai.
3.  Homepage chưa giải thích rõ mục đích của ứng dụng.
4.  Tên app `CanLua` trên OAuth consent screen không khớp/không được thể
    hiện rõ trên homepage.

Phần ownership hiện đã được xử lý bằng Google Search Console.

Cần viết lại homepage để xử lý các vấn đề còn lại.

------------------------------------------------------------------------

## 3. Yêu cầu bắt buộc đối với homepage

Theo yêu cầu của Google OAuth verification, homepage phải:

-   Nhận diện rõ ứng dụng/brand.
-   Mô tả đầy đủ mục đích và chức năng chính của ứng dụng.
-   Giải thích minh bạch mục đích yêu cầu dữ liệu Google.
-   Public và truy cập được mà không cần login.
-   Có liên kết trực tiếp, dễ nhìn thấy tới Privacy Policy.
-   Privacy Policy link trên homepage phải khớp với URL đã khai báo
    trong OAuth consent screen.
-   Không redirect homepage sang domain/URL khác.

Privacy Policy chính xác của CanLua:

`https://nhthien68.github.io/privacy-policy/app-can-lua/`

------------------------------------------------------------------------

## 4. Nội dung chính của trang

### Hero / App introduction

Phải hiển thị rõ:

**CanLua**

Ngay phần đầu trang cần có một đoạn giới thiệu ngắn về CanLua.

Không tự bịa chức năng nếu source code/repository hiện tại đã có thông
tin chính xác về ứng dụng.

Nếu chưa đủ thông tin để xác định chức năng thật của CanLua, hãy đánh
dấu nội dung cần bổ sung thay vì mô tả sai.

Ví dụ cấu trúc:

> CanLua is an application designed to \[MÔ TẢ CHỨC NĂNG THẬT CỦA
> CANLUA\].

Sau đó mô tả thêm các chức năng chính để một người chưa từng biết CanLua
vẫn hiểu app dùng để làm gì.

### Google Sign-In / Google user data

Tạo section rõ ràng, ví dụ:

**Google Sign-In & Data Usage**

Giải thích rằng CanLua sử dụng Google Sign-In để xác thực/đăng nhập
người dùng, nếu đúng với implementation thực tế.

Nếu app chỉ request các scope cơ bản như:

-   `openid`
-   `email`
-   `profile`

thì mô tả theo hướng:

> CanLua uses Google Sign-In to authenticate users. When you choose to
> sign in with Google, CanLua may receive basic account information
> authorized by you, such as your name, email address, and profile
> information. This information is used only for authentication and
> account-related functionality.

Chỉ liệt kê dữ liệu/scopes mà application thực sự request.

**Không được tự thêm Gmail, Google Drive, Calendar hoặc bất kỳ Google
API/data nào mà application không sử dụng.**

Nếu source code cho thấy scopes khác, hãy điều chỉnh nội dung theo
implementation thực tế.

### Privacy Policy

Có CTA/link dễ nhìn thấy:

**View CanLua Privacy Policy**

trỏ chính xác tới:

`/privacy-policy/app-can-lua/`

hoặc absolute URL tương đương:

`https://nhthien68.github.io/privacy-policy/app-can-lua/`

Link này phải xuất hiện rõ trên homepage, không được giấu trong nội dung
khó tìm.

### Other applications

Website hiện có Privacy Policy cho nhiều app:

-   CanLua
-   Quay So
-   Battery Alert

Có thể giữ section **Other Applications / Privacy Policies**, nhưng
**CanLua phải là ứng dụng nổi bật/chính của homepage** vì URL này đang
được sử dụng làm homepage trong Google OAuth verification của CanLua.

------------------------------------------------------------------------

## 5. Footer

Footer nên có tối thiểu:

-   `CanLua`
-   Link `Privacy Policy`
-   Contact/support nếu repository hiện tại đã có thông tin liên hệ
    chính xác.

Không tự tạo email, công ty, địa chỉ hoặc thông tin pháp lý không tồn
tại.

------------------------------------------------------------------------

## 6. SEO / HTML metadata

Cập nhật metadata phù hợp:

``` html
<title>CanLua - Official App Homepage</title>
<meta name="description" content="Official homepage of CanLua. Learn about the application, Google Sign-In data usage, and privacy policy.">
```

Có thể thêm Open Graph metadata nếu phù hợp.

Đảm bảo HTML semantic:

-   một `<h1>` chính chứa `CanLua`
-   section dùng `<h2>`
-   link dùng `<a href="...">`
-   có `<main>`, `<header>`, `<footer>` phù hợp.

------------------------------------------------------------------------

## 7. UI/UX

Giữ giao diện:

-   đơn giản
-   chuyên nghiệp
-   responsive mobile/desktop
-   load nhanh
-   không cần framework nếu website hiện tại là static HTML/CSS
-   không cần login
-   không cần JavaScript phức tạp
-   không popup che nội dung
-   không redirect tự động

Ưu tiên static HTML/CSS để Google crawler có thể đọc nội dung trực tiếp.

------------------------------------------------------------------------

## 8. Không được làm

Không:

-   đổi homepage thành trang login;
-   yêu cầu người dùng login mới xem được nội dung;
-   redirect homepage sang app khác;
-   dùng file Google Search Console verification làm homepage;
-   xóa file `google2e5512bfb11e6647.html`;
-   thay đổi đường dẫn Privacy Policy hiện tại của CanLua;
-   tự bịa chức năng của CanLua;
-   tự bịa dữ liệu Google mà CanLua truy cập;
-   tự bịa email/contact/company;
-   thêm các Google scopes không tồn tại;
-   đổi tên `CanLua` thành tên khác.

------------------------------------------------------------------------

## 9. File Search Console verification

File:

`google2e5512bfb11e6647.html`

phải được giữ nguyên tại root hiện tại để duy trì Search Console
ownership verification.

Không chỉnh sửa, rename hoặc xóa file này.

------------------------------------------------------------------------

## 10. Tiêu chí nghiệm thu

Sau khi sửa, truy cập:

`https://nhthien68.github.io/privacy-policy/`

phải có thể xác nhận ngay, không cần login:

1.  Đây là homepage của **CanLua**.
2.  CanLua dùng để làm gì.
3.  Các chức năng chính của CanLua.
4.  CanLua sử dụng Google Sign-In như thế nào.
5.  Google user data nào được sử dụng và dùng cho mục đích gì.
6.  Có link rõ ràng tới:
    `https://nhthien68.github.io/privacy-policy/app-can-lua/`
7.  Tên app trên trang là chính xác **CanLua**.
8.  Trang không redirect.
9.  Nội dung quan trọng có trong HTML render ban đầu.
10. Existing privacy-policy pages của các app khác vẫn hoạt động.

------------------------------------------------------------------------

## 11. Yêu cầu cho AI thực hiện

Hãy:

1.  Đọc `index.html` hiện tại và các CSS/assets liên quan trước khi sửa.
2.  Kiểm tra repository để xác định mô tả/chức năng thật của CanLua nếu
    thông tin đó có sẵn.
3.  Giữ lại style/assets có thể tái sử dụng.
4.  Viết lại `index.html` theo các yêu cầu trên.
5.  Không làm hỏng các route:
    -   `/privacy-policy/app-can-lua/`
    -   `/privacy-policy/app-quay-so/`
    -   `/privacy-policy/app-battery-alert/`
6.  Không xóa Search Console verification file.
7.  Sau khi sửa, review lại HTML theo checklist nghiệm thu ở trên.
8.  Trả về file `index.html` hoàn chỉnh và liệt kê ngắn gọn những thay
    đổi đã thực hiện.

## 12. Tham chiếu Google

Các yêu cầu trên dựa trên hướng dẫn **Google OAuth App Homepage**.
Google yêu cầu homepage nhận diện chính xác app/brand, mô tả chức năng,
giải thích mục đích yêu cầu user data, nằm trên verified domain, public
không cần login và có link tới Privacy Policy khớp với consent screen.
