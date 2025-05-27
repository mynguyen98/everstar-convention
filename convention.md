# ✅ TEAM WORKFLOW CHECKLIST

---

## 🔧 1. Quy Tắc Làm Việc Chung

- [ ] Thống nhất naming convention cho ticket và commit.
- [ ] Mọi thành viên nắm rõ quy trình ticket và code review.
- [ ] Giao tiếp và trao đổi rõ ràng, trực tiếp nếu cần.

---

## 📌 2. Ticket Management (Jira)

### 📄 Viết Ticket

- [ ] Tên ticket đúng cấu trúc:  
       `[TICKET cha][FE/BE][CD/Task/Bug][Common/screen] mô tả`  
       _Ví dụ: `[FAN-4][FE][CD][Common] Setup prettier, lint, husky`_
- [ ] Short Description để support report.

### 🧾 Mô Tả Ticket

- [ ] **Description** – mô tả nội dung công việc.
- [ ] **Requirement** – đầu ra cụ thể cần đạt được.
- [ ] **Notes** _(nếu có)_ – các lưu ý đặc biệt.

### 🔗 Gán Ticket

- [ ] Assign đúng người thực hiện.
- [ ] Link ticket cha/con rõ ràng.

---

## 🧪 3. Quy Trình Review Ticket

### 🔍 Ticket Review

- [ ] Gắn reviewer cho ticket.
- [ ] Reviewer kiểm tra → gắn lại người thực hiện nếu có vấn đề.
- [ ] Fix xong → gắn lại reviewer lần 2.
- [ ] Đạt yêu cầu → người làm task tự close ticket.

### 🐞 Bug Handling

- [ ] Log bug riêng biệt (ticket riêng).
- [ ] Pull request được gắn trong comment.
- [ ] Tag người review fix bug.
- [ ] Sau khi fix, gán lại người report để retest.
- [ ] Xác nhận OK thì close.

---

## 🧱 4. Commit & Precommit Rules

### ✏️ Commit Message

- [ ] Đúng format:  
       `type: [TICKET][Position][Task][common/screen] message`  
       _Ví dụ: `feat: [FAN-4][FE][CD][Home] Setup header UI`_

### ✅ Precommit Check

- [ ] Husky setup hoạt động.
- [ ] Lint / Format / Test pass khi commit.

---

## 🔀 5. Quy Trình Pull Request & Merge

- [ ] PR có mô tả rõ ràng (mục tiêu, ảnh, hướng dẫn test...).
- [ ] Tối thiểu 2 reviewer (luân phiên).
- [ ] Chia commit hợp lý, không gộp commit lớn.
- [ ] PR đã pass CI/CD hoặc pre-check.
- [ ] Có gắn link Jira hoặc ticket cha.

---

## 💻 6. Code Quality Checklist

### 📁 Structure & Component

- [ ] Component chia nhỏ hợp lý.
- [ ] Tránh render thừa / rerender không cần thiết.
- [ ] Logic có thể tách ra hook nếu dùng lại.

### 🎨 UI/UX

- [ ] UI bám sát thiết kế gốc.
- [ ] Kiểm tra responsive, khoảng cách, alignment.

### ⚙️ Logic & Hook

- [ ] Đúng với yêu cầu nghiệp vụ.
- [ ] Có xử lý `try/catch`, fallback UI khi lỗi.
- [ ] Sử dụng hook đúng cách, tránh overuse hoặc misuse.
- [ ] Có tối ưu hiệu năng (memo, lazy load, debounce… nếu cần).

---

## 🌿 12. Branch Naming Convention

- [ ] Đặt tên nhánh theo chuẩn:  
       `feature/parentBranch-childTicket-message` (cho feature)  
       `feature/parentBranch-childTicket-message` (cho ticket con)  
       `fixbug/parentBranch-childTicket-message`  
       `hotfix/parentBranch-childTicket-message`  
       `release/vX.Y.Z` (cho release)

- 📌 Ví dụ:

  - `feature/dev-FAN-3-config-lint`
  - `release/v1.2.0`

- 🧠 Tips:
  - Dùng chữ thường, gạch nối `-` giữa các từ.
