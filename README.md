```text
com.example.restaurant
│
├── core/                           # CÁC THÀNH PHẦN DÙNG CHUNG (Core Layer)
│   ├── base/                       # Các lớp cơ sở (Base Classes)
│   │   ├── BaseActivity.java       # Activity cha (xử lý toolbar, loading, show toast chung)
│   │   └── BaseFragment.java       # Fragment cha (xử lý binding, context chung)
│   │
│   ├── session/                    # Quản lý phiên làm việc
│   │   └── SessionManager.java     # Lưu trạng thái đăng nhập (SharedPreferences), check quyền (Role)
│   │
│   └── utils/                      # Các tiện ích hỗ trợ (Utilities)
│       ├── Constants.java          # Chứa hằng số (DATABASE_NAME, API_KEY, Intent Keys)
│       ├── DateUtils.java          # Format ngày tháng (dd/MM/yyyy)
│       ├── PriceUtils.java         # Format tiền tệ (VND), tính toán tổng tiền
│       ├── RoleUtils.java          # Kiểm tra quyền hạn User
│       └── ValidationUtils.java    # Kiểm tra form (email, pass, phone hợp lệ)
│
├── data/                           # TẦNG DỮ LIỆU (Data Layer - Room Database)
│   ├── model/                      # Thực thể (Entities) - Ánh xạ 1:1 với bảng CSDL
│   │   ├── User.java               # Bảng người dùng
│   │   ├── ... (Các model khác tương ứng với bảng DB)
│   │   └── PaymentMethod.java
│   │
│   ├── database/                   # Cấu hình Database
│   │   ├── AppDatabase.java        # Class khởi tạo Room DB, migrate version
│   │   ├── UserDao.java            # DAO: Các câu lệnh truy vấn SQL cho bảng User
│   │   ├── ... (Các DAO khác)
│   │   └── PaymentMethodDao.java
│   │
│   └── repository/                 # Kho chứa dữ liệu (Repository Pattern)
│       ├── AuthRepository.java     # Xử lý logic đăng nhập/đăng ký, gọi xuống DAO
│       ├── ... (Các Repo khác)
│       └── NotificationRepository.java
│
├── ui/                             # TẦNG GIAO DIỆN (Presentation Layer)
│   ├── auth/                       # Màn hình xác thực
│   │   ├── LoginActivity.java      # Màn hình Đăng nhập
│   │   └── RegisterActivity.java   # Màn hình Đăng ký
│   │
│   ├── customer/                   # GIAO DIỆN KHÁCH HÀNG
│   │   ├── home/                   # Trang chủ khách hàng
│   │   ├── menu/                   # Xem danh sách món ăn, tìm kiếm
│   │   ├── cart/                   # Giỏ hàng, xác nhận đặt món
│   │   ├── order/                  # Lịch sử đơn hàng đã đặt
│   │   └── reservation/            # Màn hình đặt bàn trước
│   │
│   ├── staff/                      # GIAO DIỆN NHÂN VIÊN
│   │   ├── home/                   # Dashboard cho nhân viên
│   │   ├── order/                  # Quản lý đơn hàng (Tiếp nhận/Từ chối/Hoàn thành)
│   │   └── table/                  # Sơ đồ bàn, cập nhật trạng thái bàn (Trống/Có khách)
│   │
│   └── owner/                      # GIAO DIỆN QUẢN LÝ (CHỦ QUÁN)
│       ├── home/                   # Dashboard tổng quan
│       ├── menu/                   # Quản lý thực đơn (Thêm/Sửa/Xóa món)
│       ├── staff/                  # Quản lý nhân viên
│       └── report/                 # Báo cáo doanh thu, thống kê
│
└── MyApplication.java              # Application Class (Khởi tạo DB, Context toàn cục)
