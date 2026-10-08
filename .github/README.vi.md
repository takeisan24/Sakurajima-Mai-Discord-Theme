<p align="center">
  <img src="../image/preview/main.jpg" width="860" alt="Theme Sakurajima Mai: khung chat, danh sách kênh và danh sách thành viên trên nền hình Mai">
</p>

<h1 align="center">Sakurajima Mai Theme</h1>

<p align="center">
  Theme Discord tông lavender dịu nhẹ lấy cảm hứng từ Sakurajima Mai (<i>Seishun Buta Yarou</i>),<br>
  xây dựng trên nền <a href="https://github.com/puckzxz/NotAnotherAnimeTheme">NotAnotherAnimeTheme</a> của puckzxz.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-3.9.0-a895d6?style=flat-square" alt="Phiên bản">
  <img src="https://img.shields.io/badge/Vencord-supported-a895d6?style=flat-square" alt="Hỗ trợ Vencord">
  <img src="https://img.shields.io/badge/BetterDiscord-supported-a895d6?style=flat-square" alt="Hỗ trợ BetterDiscord">
  <img src="https://img.shields.io/badge/license-Unlicense-e0b494?style=flat-square" alt="Unlicense">
</p>

<p align="center">
  <a href="README.md">English</a> · <b>Tiếng Việt</b>
</p>

---

## Tính năng

- **Phong cách kính cân bằng:** hình nền vẫn hiện sau thanh bên và khung chat, lớp kính tối giữ chữ dễ đọc. Popout, menu, tooltip và modal đặc 100% nên không bao giờ lẫn vào nền.
- **Bảng màu Lavender Dusk:** lavender tím và màu đào sứ lấy từ chính hình nền, trên các lớp nền tối cùng tông. Chỉ một khối biến là đổi màu được cả theme.
- **Dựa trên design token của Discord:** menu, popout, tooltip, modal, bộ chọn và các màn hình phụ (Discovery, Shop, Quests, Stage, Onboarding...) đều được tô qua các biến Discord thật sự dùng, nên trụ được qua phần lớn các bản cập nhật Discord.
- **Màu có ý nghĩa rõ ràng:** lavender là chưa đọc hoặc đang chọn, hồng mauve là được nhắc tên (mention), đỏ giữ cho thao tác nguy hiểm và mic tắt, xanh lá cho "đang nói" và "đã kết nối".
- **Tương tác nhỏ, êm:** vạch sáng khi hover, server nhấc nhẹ, gạch chân link trượt, reaction nảy nhẹ. Không có gì lặp vô hạn ngoài hình nền.
- **Chữ ký chú thỏ:** logo thỏ lavender trên thanh tiêu đề, tên server chuyển màu, khía kim cương ở kênh chưa đọc và icon kẹp tóc thỏ ở nút Home.
- **Thân thiện với plugin:** BetterFolders, ShikiCodeblocks, RoleColorEverywhere... giữ nguyên màu của chúng, kèm công tắc một dòng nếu bạn muốn dùng màu Mai.
- **Hỗ trợ trợ năng:** tôn trọng cài đặt Reduced Motion, High Contrast, Saturation của Discord, chế độ High Contrast của Windows và tùy chọn giảm chuyển động của hệ điều hành (hình nền tĩnh). Chữ và nút chính đạt độ tương phản WCAG AA.

## Xem trước

| Popout hồ sơ | Menu |
|---|---|
| <img src="../image/preview/profile.jpg" width="300" alt="Popout hồ sơ theo bảng màu Mai"> | <img src="../image/preview/menu.jpg" width="300" alt="Menu server với mục chọn lavender"> |

## Cài đặt

### Vencord / Vesktop

**Cách A: link online (tự cập nhật)**

1. Mở **User Settings → Vencord → Themes → Online Themes**.
2. Dán link này:
   ```
   https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/SakurajimaMai.theme.css
   ```

**Cách B: file trên máy**

1. Tải [`SakurajimaMai.theme.css`](https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/SakurajimaMai.theme.css).
2. Mở **User Settings → Vencord → Themes → Open Themes Folder** và chép file vào đó.
3. Bật **Sakurajima Mai Theme** trong danh sách theme.

### BetterDiscord

1. Tải [`SakurajimaMai.theme.css`](https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/SakurajimaMai.theme.css).
2. Mở **User Settings → Themes → Open Themes Folder** (thường là `%AppData%\BetterDiscord\themes`) và chép file vào đó.
3. Bật **Sakurajima Mai Theme**.

> Theme luôn hiển thị giao diện Mai tối, dù bạn chọn giao diện nào của Discord (Dark, Ash, Onyx, Light hay theme màu Nitro), nên không bị xung đột.

## Tùy chỉnh

**Đừng** sửa trực tiếp file theme vì nó bị thay mới mỗi lần theme cập nhật. Hãy đặt phần tùy chỉnh vào **QuickCSS** (Vencord: *Themes → Edit QuickCSS*; BetterDiscord: *Custom CSS*) để giữ được qua các bản cập nhật.

Chép các biến bạn muốn đổi, ví dụ:

```css
:root {
  /* Hình nền. Các bản GIF Mai có sẵn:
     maisan-soft.gif (mặc định), maisan.gif (bản gốc, rực hơn),
     maisan-silhouette.gif (bóng tối, dễ đọc nhất).
     Hoặc bất kỳ link .jpg / .png / .gif nào của bạn. */
  --theme-background-image: url("https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/image/maisan.gif") !important;

  /* Lớp kính phủ toàn app. Số càng nhỏ, hình nền càng rõ.
     Trong hơn: 0.30   Mặc định: 0.42   Dễ đọc hơn: 0.60 */
  --theme-transparency: rgb(var(--sm-glass-rgb) / 0.42) !important;

  /* Kính phủ thêm riêng cho khung chat, nơi chữ nằm đè lên Mai.
     0.15 = mặc định (hình nền dịu), 0.35 = nên dùng với hình nền gốc */
  --sm-chat-glass: 0.15 !important;

  /* Đường phân cách lavender quanh khung chat (0 để ẩn) */
  --sm-separator-alpha: 0.6 !important;

  /* Độ mờ sau bảng người dùng góc dưới trái (0px để tắt) */
  --sm-panel-blur: 10px !important;
}
```

### Tất cả các biến

| Biến | Mặc định | Tác dụng |
|---|---|---|
| `--theme-background-image` | `maisan-soft.gif` | Hình nền. Có sẵn thêm: `maisan.gif` (gốc), `maisan-silhouette.gif` |
| `--sm-wallpaper-color` | `#302e34` | Màu quanh hình nền và lúc hình đang tải |
| `--sm-wallpaper-reduced-motion` | `maisan-soft-static.png` | Ảnh tĩnh dùng khi bật giảm chuyển động. Nếu thay hình nền, hãy đặt ảnh tĩnh của bạn vào đây |
| `--sm-wallpaper-position`, `--sm-wallpaper-size` | `center`, `cover` | Vị trí hình nền (ví dụ `right bottom` / `auto 100%` cho ảnh nhân vật đã tách nền) |
| `--sm-glass-rgb` | `20 19 24` | Màu của mọi lớp kính |
| `--theme-transparency` | `rgb(var(--sm-glass-rgb) / .42)` | Lớp kính phủ toàn app |
| `--sm-chat-glass` | `0.15` | Kính phủ thêm cho khung chat và danh sách bạn bè (giữ chữ dễ đọc trên hình Mai) |
| `--message-box-transparency` | `rgb(var(--sm-glass-rgb) / .48)` | Kính của ô nhập tin nhắn và bảng người dùng |
| `--sm-panel-blur` | `10px` | Độ mờ sau bảng người dùng |
| `--sm-separator-alpha` | `0.6` | Đường phân cách lavender quanh khung chat (`0` để ẩn) |
| `--sm-accent` + `--sm-accent-rgb` | `#a895d6` / `168 149 214` | Màu nhấn chính (hover, làm nổi, mục đang chọn). **Đổi cả hai cùng lúc.** |
| `--sm-accent-strong` (+ `-hover`, `-active`) | `#7d68b8` | Nút đặc, công tắc, huy hiệu. Giữ đủ tối để chữ trắng dễ đọc. |
| `--sm-accent-2` + `--sm-accent-2-rgb` | `#e8bf9f` / `232 191 159` | Màu nhấn phụ (link, thanh cuộn, code inline). **Đổi cả hai cùng lúc.** |
| `--sm-mention` + `--sm-mention-rgb` | `#b9487f` / `185 72 127` | Mention: tin nhắn nhắc bạn, huy hiệu mention, chấm thông báo. **Đổi cả hai cùng lúc.** |
| `--sm-surface-0` … `--sm-surface-3` | `#16151a` … `#28262d` | Nền đặc của popout, menu, tooltip, modal |
| `--sm-text`, `--sm-text-strong`, `--sm-text-subtle`, `--sm-text-muted` | `#f4f2f6`, `#fff`, `#d3d0dc`, `#a9a6b2` | Màu chữ |
| `--sm-nitro-profiles` | `native` | `native` giữ màu hồ sơ Nitro của người khác, `mai` vẽ lại mọi hồ sơ theo bảng màu Mai |
| `--sm-role-mentions` | `native` | `mai` tô lại mention màu role của RoleColorEverywhere bằng màu mention của Mai |
| `--sm-codeblocks` | `native` | `mai` đặt khối code ShikiCodeblocks lên nền Mai (màu cú pháp giữ nguyên) |
| `--sm-radius-menu` | `12px` | Độ bo góc menu chuột phải |
| `--sm-logo-mask` | SVG đầu thỏ | Hình logo trên thanh tiêu đề (SVG/PNG bất kỳ làm mask, tô bằng `--sm-accent`) |
| `--home-icon-image`, `--home-icon-image-zoom`, `--home-icon-image-position` | Kẹp tóc thỏ, `82%`, `center` | Icon nút Home |
| `--server-listing-width` | `72px` | Độ rộng danh sách server (từ nền NotAnotherAnimeTheme) |

## Hành vi với Nitro

| Tính năng Nitro | Hành vi |
|---|---|
| **Client theme** (dải màu app của riêng bạn) | Bị vô hiệu để hình nền Mai hiện ra |
| **Profile theme** (màu popout và hồ sơ của người khác) | **Giữ đúng như chủ hồ sơ đã chọn**, kèm viền lavender. Hồ sơ không có theme Nitro dùng bảng màu Mai đặc |

Muốn mọi hồ sơ đều theo bảng màu Mai? Thêm dòng này vào QuickCSS:

```css
:root { --sm-nitro-profiles: mai !important; }
```

## Tương thích plugin

Mặc định màu của plugin luôn được ưu tiên: theme chỉ đóng khung, không bao giờ tô lại.

| Plugin | Trạng thái | Ghi chú |
|---|---|---|
| **BetterFolders** | ✅ Hỗ trợ | Thanh folder có cùng chấm chưa đọc, vòng chọn và huy hiệu như danh sách server. Giữ nguyên màu folder của bạn |
| **ShikiCodeblocks** | ✅ Hỗ trợ | Khối code có viền lavender nhẹ. Chọn theme cú pháp trong cài đặt plugin: **RosePineMoon** và **CatppuccinMocha** hợp với bảng màu. `--sm-codeblocks: mai` đặt khối code lên nền Mai |
| **RoleColorEverywhere** | ✅ Hỗ trợ | Giữ màu role trên tên và @mention. `--sm-role-mentions: mai` tô lại mention bằng màu mention của Mai |
| **MemberCount**, **ServerListIndicators**, **PlatformIndicators**, **TypingIndicator** | ✅ Hỗ trợ | Dùng token của Discord nên tự theo bảng màu |
| **FakeNitro**, **Decor** (khung avatar) | ✅ Hỗ trợ | Hình ảnh Nitro hoạt động như mục [Hành vi với Nitro](#hành-vi-với-nitro) |

Bật cả hai công tắc:

```css
:root {
  --sm-role-mentions: mai !important;
  --sm-codeblocks: mai !important;
}
```

## Hiệu năng và máy cấu hình yếu

Hình nền là ảnh GIF động, cũng là thứ duy nhất khiến GPU phải làm việc liên tục. Trên máy yếu:

```css
:root {
  /* Hình nền tĩnh (cùng ảnh mà chế độ Reduced Motion dùng) */
  --theme-background-image: url("https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/image/maisan-soft-static.png") !important;
  /* Tắt hiệu ứng mờ sau bảng người dùng */
  --sm-panel-blur: 0px !important;
}
```

Bật **User Settings → Accessibility → Reduced Motion** trong Discord (hoặc giảm chuyển động trong hệ điều hành) sẽ tự làm điều tương tự, đồng thời tắt mọi hiệu ứng hover.

## Xử lý sự cố

- **Theme không cập nhật:** stylesheet nền được phục vụ qua jsDelivr, có thể bị cache một lúc. Nhấn <kbd>Ctrl</kbd>+<kbd>R</kbd> để tải lại Discord.
- **Biến trong QuickCSS không có tác dụng:** thêm `!important` như trong ví dụ để ghi đè giá trị mặc định của theme.
- **Giao diện bị lỗi sau khi Discord cập nhật:** mở [issue](https://github.com/takeisan24/Sakurajima-Mai-Discord-Theme/issues) kèm ảnh chụp màn hình.
- **Lỗi ở danh sách server hoặc bố cục nền:** có thể do nền NotAnotherAnimeTheme. Xem [issues](https://github.com/puckzxz/NotAnotherAnimeTheme/issues) hoặc [server hỗ trợ](https://discord.gg/FdZhbjY) của dự án gốc.

## Lịch sử phiên bản

Xem mục **Changelog** trong [README tiếng Anh](README.md#changelog).

## Cấu trúc dự án

| Đường dẫn | Thuộc về | Mục đích |
|---|---|---|
| `SakurajimaMai.theme.css` | Theme này | Theme Sakurajima Mai |
| `image/maisan*.gif`, `image/maisan-soft-static.png`, `image/bunny-hairpin.*` | Theme này | Hình nền (gốc, dịu, bóng tối, tĩnh) và icon Home |
| `image/preview/` | Theme này | Ảnh chụp cho README |
| `.github/README.md`, `.github/README.vi.md` | Theme này | Trang này (tiếng Anh và tiếng Việt) |
| `css/v3/`, `build/v3/` | NotAnotherAnimeTheme | Stylesheet nền mà theme import |
| `NotAnotherAnimeTheme.theme.css`, `README.md`, `community/`, `css/*csl.css` | NotAnotherAnimeTheme | Theme gốc, README gốc và các theme cộng đồng |

Các file thuộc NotAnotherAnimeTheme được giữ y hệt bản gốc, để có thể gộp các bản sửa từ upstream mà không bị xung đột. README của dự án gốc là [`README.md`](../README.md).

## Ghi công

- **[puckzxz](https://github.com/puckzxz)**: tác giả [NotAnotherAnimeTheme](https://github.com/puckzxz/NotAnotherAnimeTheme), nền tảng của theme này. Nếu bạn thích, hãy cân nhắc [ủng hộ tác giả gốc](https://www.paypal.me/ChrisBock).
- **[V-X](https://github.com/ImVexed)** và **[Qu4k3](https://github.com/Qu4k3)**: lưu trữ CDN và hỗ trợ lâu dài cho NotAnotherAnimeTheme.
- **[takeisan24](https://github.com/takeisan24)**: theme Sakurajima Mai, bảng màu, tích hợp hình nền và icon Home.
- Sakurajima Mai và *Seishun Buta Yarou* thuộc về Hajime Kamoshida, Keji Mizoguchi và các nhà phát hành. Đây là theme fan làm, phi thương mại.

## Giấy phép

Phát hành vào phạm vi công cộng theo [The Unlicense](../LICENSE), giống NotAnotherAnimeTheme.
