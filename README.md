# Term Project Web App for a Real Person
**Course** 953104 Web User Interface Design and Development (Semester 1/2026)  
**Live Demo Website**: [https://wa-shi.github.io/BAS-website-953104/](https://wa-shi.github.io/BAS-website-953104/)

---

##  Team Information
- **Partner 1**  [Student Name 1] (Student ID  [ID 1])
- **Partner 2**  [Student Name 2] (Student ID  [ID 2])
- **Section**  [Section Number]

---

##  User & Problem Statement
- **Real User**  บริษัท บิวดิ้ง แอดวานซด์ โซลูชั่น จำกัด (Building Advanced Solution Co., Ltd. - BAS) ผู้เชี่ยวชาญด้านระบบวิศวกรรมอาคารอัตโนมัติ (BMS) และความปลอดภัย
- **Their Problem**  ลูกค้าที่ต้องการติดตั้งระบบวิศวกรรมอาคารขนาดใหญ่เข้าถึงข้อมูลบริการและส่งข้อมูลขอนัดหมายสำรวจหน้างานได้ยาก ขาดระบบหน้าเว็บแบบ Single-Page ที่กระชับ โหลดเร็ว และไม่ต้องการระบบเซิร์ฟเวอร์ซับซ้อน
- **Solution Overview**  เว็บไซต์ Single-Page Interactive Application พัฒนาด้วย Pure HTML5, CSS3 และ Vanilla ES6 JavaScript นำเสนอ 10 ระบบบริการหลัก ค้นหาและกรองบริการ พร้อมระบบนัดหมายสำรวจหน้างานและแบบฟอร์มตรวจสอบความถูกต้องในตัว
- **User Feedback**  "หน้าเว็บโหลดรวดเร็ว ค้นหาระบบบริการได้ง่าย และการแสดงผลสวยงามตรงตามเอกลักษณ์ของบริษัท BAS"

---

##  Feature Ownership Map

| # | Feature Name | Owner | File & Line Range | Summary |
| :- | :--- | :--- | :--- | :--- |
| 1 | Semantic HTML & Accessibility | Shared | `index.html`: L1-L530 | Semantic structural landmarks (`<header>`, `<main>`, `<section>`, `<footer>`, `<dialog>`), labels, descriptive alt tags |
| 2 | Responsive Layout | Shared | `css/style.css`: L1-L1650 | Flexbox/Grid responsive layout, mobile ($\le 480\text{px}$) & desktop ($\ge 1024\text{px}$), mobile nav fix, expand/collapse |
| 3 | Data Array & `render()` | Partner A / B | `js/app.js`: L185-L430 | In-memory 10 real service items, centralized `renderServices()` with container reset & DOM creation |
| 4 | Form Validation | Partner A / B | `js/app.js`: L680-L800 | Prevent default & inline red error messages next to inputs |
| 5 | Dynamic List & Delegation | Partner A / B | `js/app.js`: L430-L520 | Event delegation (`e.target.closest()`) + Search/Filter/Sort |
| 6 | Native Modal `<dialog>` | Partner A / B | `js/app.js`: L530-L580 | `.showModal()` and `.close()` with Escape key listener & bilingual details |
| 7 | Keyboard Interaction | Partner A / B | `js/app.js`: L630-L650 | Shortcut hotkeys (`/` to search, `Enter` to submit, `Escape` to close) |
| + | Bilingual Switcher (TH / EN) | Shared | `js/app.js`: L15-L180, L900-L960 | In-memory centralized dictionary, 0 libraries, instant full-site translation |
| + | Scrollspy & Marquee & Count-Up | Shared | `js/app.js` & `css/style.css` | Navbar scrollspy indicator, stats counter animation, partner logo color marquee |

---

## 🧪 Test Table (Minimum 8 Tests)

| Test ID | Input / Action | Expected Result | Actual Result | Pass? |
| :--- | :--- | :--- | :--- | :--- |
| T1 | Submit empty form | Display error text beside required fields | Error text shown | Pass |
| T2 | Input name < 3 chars | Display "Name must be at least 3 characters" | Message displayed | Pass |
| T3 | Fill valid data & Submit | New item added to list, form cleared | Item rendered in list | Pass |
| T4 | Click Delete button | Item removed from list and JS array | Item removed | Pass |
| T5 | Type in Search box | Filter list by matching keyword | List filtered | Pass |
| T6 | Click Open Modal | `<dialog>` displays with backdrop | Dialog opened | Pass |
| T7 | Press `Escape` key | Modal dialog closes | Modal closed | Pass |
| T8 | Press `/` key | Search input gains focus | Input focused | Pass |
| T9 | Click TH / EN toggle button | All headings, cards, and buttons switch language | Language switched | Pass |
| T10 | Scroll up and down | Navbar highlights current visible section (Scrollspy) | Highlight follows scroll | Pass |
| T11 | Click "+ สนใจระบบนี้" | System badge appears in consultation quote box | Badge added & synced | Pass |
