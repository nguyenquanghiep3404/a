Hệ Thống Thiết Kế: "The Ethereal Navigator"

1. Tổng quan & Triết lý thiết kế (Creative North Star)

Hệ thống thiết kế này được xây dựng dựa trên triết lý "The Ethereal Navigator" (Người Dẫn Đường Thanh Tinh). Nó từ bỏ những giới hạn đóng khung cứng nhắc của các ứng dụng truyền thống, thay vào đó ưu tiên bố cục đậm chất tạp chí (editorial layout) mang lại cảm giác mượt mà, thoáng đãng và dẫn dắt thông minh.

Bằng cách tận dụng tỷ lệ chữ có độ tương phản cao và sự bất đối xứng có chủ đích, hệ thống tạo ra trải nghiệm "Giám tuyển Kỹ thuật số" (Digital Curator). Các thành phần lơ lửng như Trợ lý AI, Module tìm kiếm và Bảng điều khiển (Dropdowns) mang lại cảm giác về chiều sâu không gian, giúp giao diện không chỉ là một công cụ mà là một người bạn đồng hành tinh tế.

2. Màu sắc & Phân cấp bề mặt (Colors & Surfaces)

Chiến lược màu sắc sử dụng dải màu xanh lam sang trọng kết hợp với các tông màu trung tính kiến trúc để tạo cảm giác rộng lớn và đáng tin cậy.

Màu chủ đạo (Core Tones)

Primary-900 (Deep Anchor): #001629 — Sử dụng cho các tiêu đề chính, văn bản cần độ nhấn cao và nền chính (như Hero section).

Secondary-500 (Horizon Blue): #00658d — Sử dụng cho các thành phần tương tác (nút bấm, checkbox được chọn) và điểm nhấn thương hiệu.

Tertiary-Accent (Sunlight): #ffb870 — Dành riêng cho các điểm nhấn cực kỳ quan trọng, icon Trợ lý AI và các trạng thái đặc biệt.

Các tầng bề mặt (Surface Tiers)

Thứ tự xếp lớp từ dưới lên trên:

surface-bg: #f6fafe — Màu nền móng của toàn bộ trang web (The base canvas).

surface-low: #f0f4f8 — Nền cho các ô input, button phụ, vùng xám phân tách.

surface-highest: #dfe3e7 — Dùng cho các trạng thái hover (di chuột) trên surface-low hoặc các vạch phân cách mờ.

surface-lowest: #ffffff (Card White) — Nền trắng tinh khiết, dùng cho các thẻ thông tin (Card) nổi lên trên.

on-surface: #171c1f — Màu chữ tiêu chuẩn trên các nền sáng (Không bao giờ dùng màu đen tuyệt đối #000000).

3. Typography (Nghệ thuật chữ)

Hệ thống sử dụng phông chữ duy nhất: Plus Jakarta Sans, sự cân bằng hoàn hảo giữa tính hiện đại hình học và sự ấm áp của thiết kế tạp chí cao cấp.

Phân loại

Độ dày (Weight)

Kích thước

Chiều cao dòng (Leading)

Ứng dụng

Display (Tiêu đề lớn)

Bold (700)

text-4xl đến 5xl

110% (leading-tight)

Banner chính, thông điệp thương hiệu

Headline (Tiêu đề mục)

SemiBold (600)

text-[1.75rem]

120%

Tiêu đề của các Section (Vd: Điểm đến thịnh hành)

Body (Văn bản thường)

Medium/Regular

text-base / text-sm

140% - 160%

Nội dung đọc, thẻ mô tả

Label (Nhãn phụ)

Bold (700)

text-[10px]

120%

Tiêu đề ô input, nhãn thẻ (Viết hoa toàn bộ + Tracking rộng)

4. Các Quy Tắc Thiết Kế Cốt Lõi (The Director’s Rules)

Quy tắc 1: "No-Line" (Không đường viền)

Tuyệt đối hạn chế sử dụng đường viền 1px solid màu đậm để phân chia nội dung.

Cách làm đúng: Phân tách không gian bằng cách xếp chồng các bề mặt màu khác nhau (Ví dụ: Thẻ surface-lowest đặt trên nền surface-bg).

Trường hợp bắt buộc phải có viền (như Dropdown menu), chỉ dùng viền mờ ảo: border border-surface-highest/40 hoặc border-white/20.

Quy tắc 2: "Glass & Gradient" (Kính mờ & Chuyển sắc)

Để thổi hồn vào UI, luôn sử dụng hiệu ứng Glassmorphism (Kính mờ) cho các module nổi (Thanh tìm kiếm, Dropdown, Trợ lý AI).

Công thức: Background trong suốt (Vd: bg-white/90 hoặc bg-white/80) + backdrop-blur-xl + viền sáng nhẹ border border-white/60.

Gradient chính: Từ góc trên trái xuống góc dưới phải (bg-gradient-to-br from-primary-900 to-primary-container).

Quy tắc 3: Tonal Layering & Shadows (Đổ bóng êm ái)

Từ chối các loại bóng đổ đen kịt, bẩn mắt. Sử dụng bóng đổ xung quanh (Ambient Shadow) tông lạnh.

Shadow Ethereal (Bóng mặc định): 0 12px 32px rgba(23, 28, 31, 0.06) — Dùng cho các thẻ (Cards), Nút nổi.

Shadow Dropdown (Bóng sâu hơn): 0 20px 50px rgba(0, 22, 41, 0.15) — Dùng cho các Menu xổ xuống, Modal để tạo khoảng cách rõ rệt với nền.

5. Hệ thống Component (UI Elements)

A. Nút bấm (Buttons) & Nav Pills

Nút Primary: Nền secondary-500 hoặc primary-900, chữ trắng, bo tròn lớn rounded-xl hoặc rounded-full, padding rộng (Vd: px-8 py-4). Khi hover, màu nền đảo ngược.

Nav Pills (Thanh điều hướng): - Đang chọn (Active): Kính mờ bg-white/10 backdrop-blur-md border border-white/20.

Chưa chọn (Inactive): Chữ hơi mờ text-white/70 hover:bg-white/5.

B. Form Inputs (Ô nhập liệu)

Mặc định: Nền surface-low, bo tròn rounded-[1rem], không có đường viền.

Tương tác: Khi trỏ chuột (hover) hoặc focus, đổi nền sang surface-highest hoặc thêm viền ring-2 ring-secondary-500/20.

Lấy Icon làm điểm neo bên trái (Màu text-on-surface/50, đổi sang secondary-500 khi tương tác).

C. Custom Checkbox (Nút kiểm tùy chỉnh)

Không dùng giao diện mặc định của trình duyệt.

Vuông bo góc mềm: w-5 h-5 rounded-md bg-surface-low border-2 border-transparent.

Khi checked: Nền đổi sang secondary-500, xuất hiện dấu tick trắng.

D. Trợ lý AI (AI Floating Assistant)

Đặt góc dưới cùng bên phải (bottom-10 right-10, z-50).

Biểu tượng mảng màu Tertiary (#ffb870).

Bao gồm hiệu ứng animate-pulse đằng sau (tỏa sáng nhẹ) và một Tooltip dạng Glassmorphism trượt ra khi hover.

6. Layout & Grid (Bố cục)

Bo góc (Border Radius): Ưu tiên các bo góc lớn để tạo sự mềm mại. Thường dùng rounded-[1.5rem] (24px) cho các thẻ lớn, rounded-[2rem] cho phần bo của nền chính, và rounded-[1rem] (16px) cho thẻ nhỏ.

Bất đối xứng (Asymmetry): Để phá vỡ cảm giác rập khuôn, thỉnh thoảng sử dụng cấu trúc lưới 2 cột hoặc 3 cột không đều (VD: Cột trái lớn, 2 cột nhỏ bên phải; hoặc 2 item dòng trên, 3 item dòng dưới như phần Chùm ảnh Phú Quốc).

7. Các quy tắc NÊN và KHÔNG NÊN (Do's and Don'ts)

✅ NÊN (DO):

NÊN cung cấp khoảng trắng theo chiều dọc (Vertical whitespace) đủ lớn giữa các section (Ví dụ: py-12 hoặc py-16) để mắt người dùng được nghỉ ngơi.

NÊN dùng hiệu ứng animate-in fade-in slide-in-from-top-2 duration-200 khi xuất hiện Dropdown/Modal để tạo cảm giác mượt mà.

NÊN sử dụng thẻ label-sm in hoa, màu phụ (VD: text-[10px] text-on-surface/50 uppercase tracking-widest) để làm tiêu đề phụ cho các nhóm thông tin.

❌ KHÔNG NÊN (DON'T):

KHÔNG NÊN nhồi nhét nội dung. Nếu thông tin quá dài, hãy dùng thanh cuộn ngang (Horizontal scroll với hide-scrollbar).

KHÔNG NÊN dùng hộp thoại Alert mặc định của trình duyệt. Mọi tương tác popup phải được làm bằng Component Modal (như Modal chọn ngôn ngữ).

KHÔNG NÊN làm các nút bấm quá nhỏ. Mọi phần tử tương tác (như tăng giảm hành khách) phải đủ vùng chạm (ít nhất w-8 h-8 hoặc w-10 h-10 trên mobile).

8. Cấu hình Tailwind CSS (Sử dụng tái lập)

Sử dụng đoạn script này trong thẻ <head> của bất kỳ file HTML nào để tái tạo lại toàn bộ bảng màu và hệ thống bóng đổ của Ethereal Navigator:

tailwind.config = {
    theme: {
        extend: {
            fontFamily: {
                sans: ['"Plus Jakarta Sans"', 'sans-serif'],
            },
            colors: {
                primary: {
                    900: '#001629',
                    container: '#002b49'
                },
                secondary: {
                    500: '#00658d'
                },
                tertiary: {
                    accent: '#ffb870'
                },
                surface: {
                    bg: '#f6fafe',
                    low: '#f0f4f8',
                    highest: '#dfe3e7',
                    lowest: '#ffffff',
                },
                on: {
                    surface: '#171c1f'
                }
            },
            boxShadow: {
                'ethereal': '0 12px 32px rgba(23, 28, 31, 0.06)',
                'ethereal-sm': '0 4px 12px rgba(23, 28, 31, 0.04)',
                'dropdown': '0 20px 50px rgba(0, 22, 41, 0.15)',
            },
            borderRadius: {
                'DEFAULT': '1rem',
                'md': '1.5rem',
                'xl': '3rem',
            }
        }
    }
}
