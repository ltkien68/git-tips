<!-- 
  Nội dung này dùng để nhúng trực tiếp vào README.md trên GitHub.
  GitHub hỗ trợ HTML tĩnh trong Markdown, bao gồm style, table, pre, v.v.
  Lưu ý: Không sử dụng JavaScript (sẽ bị chặn).
-->

<div align="center">
  <h1>📁 Hệ thống quản lý thư mục & file chuyên nghiệp</h1>
  <p><strong>Nguyên tắc cốt lõi:</strong> <em>Mọi thứ đều có vị trí. Mọi vị trí đều có quy tắc. Mọi quy tắc đều được tự động hóa nếu có thể.</em></p>
</div>

<hr>

<h2>🗂️ 1. Cấu trúc thư mục gốc (Trên Ổ D: hoặc OneDrive)</h2>

<pre><code>D:\
├── 00_INBOX/                # Hộp thư đến tạm thời (tồn tại &lt;48h)
├── 01_WORK/                 # Công việc, học tập, dự án
├── 02_PERSONAL/             # Giấy tờ, tài chính, sức khỏe
├── 03_MEDIA/                # Ảnh, nhạc, phim, game
├── 04_SOFTWARE/             # File cài đặt, driver, tool portable
├── 05_BACKUP/               # Sao lưu từ điện thoại, ổ cứng cũ
└── 99_ARCHIVE/              # Dữ liệu &gt;1 năm không dùng nhưng không xóa
</code></pre>

<hr>

<h2>📂 2. Quy tắc đặt tên thư mục (Folder)</h2>

<h3>Công thức</h3>
<pre><code>[STT]_[TÊN_NGẮN_GỌN]          # Cấp 1
[YYYY]_[TEN_VIET_TAT]          # Cấp 2
[SO_THU_TU]_[TEN]              # Cấp 3 trở đi
</code></pre>

<h3>Nguyên tắc</h3>
<ul>
  <li>✅ Không dấu tiếng Việt</li>
  <li>✅ Không khoảng trắng (dùng <code>_</code> hoặc <code>-</code>)</li>
  <li>✅ Số thứ tự 2 chữ số (00-99) để tự động sort</li>
  <li>✅ Chữ hoa cho thư mục cấp 1, chữ thường cho cấp sâu hơn</li>
</ul>

<h3>Ví dụ</h3>
<pre><code>01_WORK/
01_WORK/2025_DoAn2/
01_WORK/2025_DoAn2/01_SourceCode/
01_WORK/2025_DoAn2/02_Document/
</code></pre>

<hr>

<h2>📄 3. Quy tắc đặt tên file (ISO 8601)</h2>

<h3>Công thức chuẩn</h3>
<pre><code>YYYY-MM-DD_TEN_FILE_MO_TA_PHIEN_BAN.duoi
</code></pre>

<h3>Chi tiết các thành phần</h3>
<table>
  <thead>
    <tr><th>Thành phần</th><th>Quy tắc</th><th>Ví dụ</th></tr>
  </thead>
  <tbody>
    <tr><td>Ngày tháng</td><td>YYYY-MM-DD (bắt buộc, để sort)</td><td><code>2025-08-15</code></td></tr>
    <tr><td>Loại file</td><td>2-3 chữ viết tắt (BC, HD, DATA)</td><td><code>BC</code> (báo cáo), <code>DATA</code> (số liệu)</td></tr>
    <tr><td>Mô tả</td><td>Không dấu, dùng <code>_</code> thay khoảng trắng</td><td><code>Do_An_2</code></td></tr>
    <tr><td>Phiên bản</td><td>vX.Y hoặc vX.Y.Z</td><td><code>v1.0</code>, <code>v2.3.1</code></td></tr>
    <tr><td>Trạng thái</td><td><code>DRAFT</code> / <code>REVIEW</code> / <code>FINAL</code> / <code>APPROVED</code></td><td><code>FINAL</code></td></tr>
    <tr><td>Đuôi file</td><td>chữ thường</td><td><code>.pdf</code>, <code>.docx</code>, <code>.xlsx</code></td></tr>
  </tbody>
</table>

<h3>Ví dụ thực tế</h3>
<pre><code># Báo cáo
2025-08-15_BC_DoAn2_DRAFT_v0.5.docx
2025-08-20_BC_DoAn2_REVIEW_v0.9.docx
2025-08-25_BC_DoAn2_FINAL_v1.0.pdf

# Số liệu Excel
2025-08-10_DATA_KhaoSat_v2.xlsx
2025-08-12_DATA_ThongKe_DATN_v1.xlsx

# Ảnh chụp màn hình
2025-08-15_1430_giao_dien_login.png
2025-08-15_1500_ket_qua_chay_code.png

# File cài đặt
7zip_v24.08_x64.exe
Python_v3.12_x64.exe

# Source code
QuanLyThuVien_v2.3.py
DoAn2_Backend_v1.0.js
</code></pre>

<h3>❌ Các kiểu đặt tên cấm kỵ</h3>
<pre><code>BaoCao.docx                     # thiếu ngày, thiếu version
Báo cáo đồ án 2 sửa lần cuối.docx  # có dấu, có khoảng trắng
final_final_final.pdf           # lặp từ final vô nghĩa
asdasd123.docx                  # vô nghĩa
</code></pre>

<hr>

<h2>🧱 4. Cấu trúc chuẩn cho một dự án (Ví dụ: Đồ án 2)</h2>

<h3>Áp dụng cho <code>01_WORK/2025_DoAn2/</code></h3>

<pre><code>2025_DoAn2/
│
├── 01_SourceCode/                     # CODE
│   ├── src/
│   ├── include/
│   ├── lib/
│   ├── .git/
│   └── README.md
│
├── 02_Document/                       # REPORT
│   ├── 01_Draft/
│   │   └── 2025-08-10_BC_DRAFT_v0.5.docx
│   ├── 02_Final/
│   │   └── 2025-08-25_BC_FINAL_v1.0.pdf
│   ├── 03_Assets/
│   │   ├── images/
│   │   └── data/
│   │       └── 2025-08-15_DATA_KhaoSat.xlsx
│   └── 04_References/
│       └── [các bài báo, sách, luận văn]
│
├── 03_Presentation/                   # Slide thuyết trình
│   ├── 2025-08-20_Slide_ThuyetTrinh_v1.pptx
│   └── 2025-08-28_Slide_ThuyetTrinh_FINAL_v2.pptx
│
└── 04_Archive/                        # Các phiên bản cũ
    ├── 2025_DoAn2_OLD_v1.zip
    └── Backup_Source_20250801.7z
</code></pre>

<hr>

<h2>🏷️ 5. Tiền tố phân loại nhanh</h2>

<table>
  <thead>
    <tr><th>Tiền tố</th><th>Ý nghĩa</th><th>Ví dụ</th></tr>
  </thead>
  <tbody>
    <tr><td><code>_</code> (underscore đầu)</td><td>File đang xử lý dở</td><td><code>_2025-08-15_dang_lam_BT.docx</code></td></tr>
    <tr><td><code>!</code></td><td>Quan trọng, khẩn cấp</td><td><code>!_2025-08-20_Lich_thi.pdf</code></td></tr>
    <tr><td><code>@</code></td><td>Tài liệu tham khảo</td><td><code>@2025-08-01_TaiLieu_OOP.pdf</code></td></tr>
    <tr><td><code>#</code></td><td>Cần thảo luận nhóm</td><td><code>#2025-08-10_Cau_hoi_Thay.docx</code></td></tr>
    <tr><td><code>~</code></td><td>File backup tạm</td><td><code>~2025-08-15_BaoCao_old.docx</code></td></tr>
  </tbody>
</table>

<hr>

<h2>🔄 6. Quy trình xử lý file mới (Workflow)</h2>

<h3>Bước 1: File mới nhận → <code>00_INBOX/</code></h3>
<pre><code>00_INBOX/
├── bao_cao_thay_giao_chua_xem.pdf
└── file_can_xu_ly.jpg
</code></pre>

<h3>Bước 2: Trong vòng 48h, phân loại</h3>
<table>
  <thead>
    <tr><th>Loại file</th><th>Chuyển đến</th></tr>
  </thead>
  <tbody>
    <tr><td>Tài liệu công việc</td><td><code>01_WORK/[du_an]/02_Document/</code></td></tr>
    <tr><td>Hóa đơn, giấy tờ</td><td><code>02_PERSONAL/Finance/2025/</code></td></tr>
    <tr><td>Ảnh, video</td><td><code>03_MEDIA/Photos/2025/</code></td></tr>
    <tr><td>File cài đặt</td><td><code>04_SOFTWARE/_Installers/</code></td></tr>
    <tr><td>Không biết để đâu</td><td><code>00_INBOX/0_Unsorted/</code> (tạm, sẽ xử lý sau)</td></tr>
  </tbody>
</table>

<h3>Bước 3: Cuối tuần dọn dẹp</h3>
<ul>
  <li>Xóa file rác, trùng lặp</li>
  <li>Nén các file cũ &gt;1 năm vào <code>99_ARCHIVE/</code></li>
</ul>

<hr>

<h2>🛠️ 7. Công cụ hỗ trợ</h2>

<h3>Windows (miễn phí, khuyên dùng)</h3>
<table>
  <thead>
    <tr><th>Tool</th><th>Công dụng</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>PowerToys PowerRename</strong></td><td>Đổi tên hàng loạt theo pattern</td></tr>
    <tr><td><strong>Everything</strong></td><td>Tìm kiếm file siêu nhanh theo tên</td></tr>
    <tr><td><strong>Directory Opus</strong> (trả phí)</td><td>Quản lý tab, bookmark, quy tắc tự động</td></tr>
    <tr><td><strong>File Juggler</strong></td><td>Tự động phân loại file theo quy tắc</td></tr>
  </tbody>
</table>

<h3>macOS</h3>
<table>
  <thead>
    <tr><th>Tool</th><th>Công dụng</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>Hazel</strong></td><td>Tự động phân loại, đổi tên, xóa</td></tr>
    <tr><td><strong>BetterTouchTool</strong></td><td>Gán phím tắt cho các thao tác file</td></tr>
  </tbody>
</table>

<h3>Terminal (Linux / macOS / WSL)</h3>
<pre><code># Đổi tên hàng loạt thêm ngày vào đầu file
for f in *.pdf; do mv "$f" "$(date +%Y-%m-%d)_$f"; done

# Tìm tất cả file có 'final' trong tên
find . -name "*final*" -type f

# Xóa file rác .DS_Store (macOS) hoặc Thumbs.db (Windows)
find . -name ".DS_Store" -delete
find . -name "Thumbs.db" -delete
</code></pre>

<hr>

<h2>📋 8. Checklist kiểm tra định kỳ (Mỗi tuần 15 phút)</h2>

<ul>
  <li>☐ <code>00_INBOX/</code> còn dưới 10 file? Nếu không → phân loại ngay.</li>
  <li>☐ Tất cả file mới đã được đặt tên theo chuẩn <code>YYYY-MM-DD_TEN_vX</code>?</li>
  <li>☐ File nào có tên chứa <code>final</code>, <code>sua</code>, <code>chinh_thuc</code> chưa? → Rename ngay.</li>
  <li>☐ File trong <code>99_ARCHIVE/</code> đã được nén (<code>.7z</code> / <code>.zip</code>) chưa?</li>
  <li>☐ Folder <code>05_BACKUP/</code> có chứa backup cũ hơn 6 tháng? → Xóa hoặc archive.</li>
  <li>☐ Trên Desktop có file hay folder gì không? → Chỉ để shortcut.</li>
</ul>

<hr>

<h2>🧠 9. Triết lý cuối cùng</h2>

<blockquote>
  <p><strong>Một cấu trúc thư mục tốt không phải là thứ bạn nhìn thấy,<br>
  mà là thứ bạn <em>không cần nhìn</em> vì bạn đã biết chính xác mọi thứ ở đâu.</strong></p>
</blockquote>

<pre><code>Quy tắc duy nhất phải nhớ:
┌─────────────────────────────────────────────────────┐
│  YYYY-MM-DD_Tên_Mô_Tả_vX.Y.duoi                     │
│  Không dấu, không cách, dùng _ thay khoảng trắng    │
└─────────────────────────────────────────────────────┘
</code></pre>

<hr>

<h2>🔗 10. Tài liệu tham khảo</h2>

<ul>
  <li><a href="https://www.iso.org/iso-8601-date-and-time-format.html">ISO 8601 Date format</a></li>
  <li><a href="https://learn.microsoft.com/en-us/windows/powertoys/powerrename">PowerToys PowerRename</a></li>
  <li><a href="https://semver.org/">Semantic Versioning</a></li>
</ul>

<hr>

<p align="center">
  <strong>📌 Version:</strong> 1.0 &nbsp;&nbsp;|&nbsp;&nbsp;
  <strong>📅 Cập nhật lần cuối:</strong> 2025-08-15 &nbsp;&nbsp;|&nbsp;&nbsp;
  <strong>✍️ Tác giả:</strong> [Tên bạn / Team của bạn]
</p>
