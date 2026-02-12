```text
app/src/main/java/com/example/restaurant/
├── 📁 core/                        # Các thành phần cốt lõi dùng chung
│   ├── 📁 base/                    # Base classes (BaseActivity, BaseFragment)
│   ├── 📁 session/                 # Quản lý phiên làm việc (SessionManager)
│   └── 📁 utils/                   # Các lớp tiện ích (Constants, Date, Price, Validation...)
│
├── 📁 data/                        # Tầng dữ liệu của ứng dụng
│   └── 📁 database/                # Room Database & Data Access Objects (DAOs)
│       ├── AppDatabase.java        # Cấu hình chính cho Room Database
│       └── 📄 (13 DAOs: Category, Order, User, Reservation...)
│
├── 📁 model/                       # Các thực thể dữ liệu (Entities)
│   └── 📄 (13 Models: MenuItem, DiningTable, Payment, Role...)
│
├── 📁 repository/                  # Tầng trung gian (Repository Pattern)
│   └── 📄 (6 Repositories: Auth, Menu, Order, Reservation...)
│
└── 📁 ui/                          # Tầng giao diện người dùng (UI)
    ├── 📁 auth/                    # Chức năng Đăng nhập & Đăng ký
    ├── 📁 customer/                # Luồng chức năng cho Khách hàng
    │   ├── 📁 cart/                # Giỏ hàng & Adapter
    │   ├── 📁 home/                # Trang chủ khách hàng
    │   ├── 📁 menu/                # Danh sách thực đơn
    │   ├── 📁 order/               # Lịch sử đơn hàng
    │   └── 📁 reservation/         # Đặt bàn
    ├── 📁 owner/                   # Luồng chức năng cho Chủ nhà hàng
    │   ├── 📁 home/                # Dashboard quản lý
    │   ├── 📁 menu/                # Chỉnh sửa & Quản lý thực đơn
    │   ├── 📁 report/              # Báo cáo & Thống kê doanh thu
    │   └── 📁 staff/               # Quản lý nhân viên
    └── 📁 staff/                   # Luồng chức năng cho Nhân viên
        ├── 📁 home/                # Trang chủ nhân viên
        ├── 📁 order/               # Quản lý đơn hàng đang xử lý
        └── 📁 table/               # Theo dõi trạng thái bàn (Table Status)
```
