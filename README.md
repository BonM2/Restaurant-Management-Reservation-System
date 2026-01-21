com.example.restaurant
│
├── core
│   ├── base
│   │   ├── BaseActivity.java
│   │   └── BaseFragment.java
│   │
│   ├── session
│   │   └── SessionManager.java      // lưu user, role, login state
│   │
│   └── utils
│       ├── Constants.java
│       ├── DateUtils.java
│       ├── PriceUtils.java
│       ├── RoleUtils.java
│       └── ValidationUtils.java
│
├── data
│   ├── model            // 1 TABLE = 1 MODEL
│   │   ├── User.java
│   │   ├── Role.java
│   │   ├── Category.java
│   │   ├── MenuItem.java
│   │   ├── DiningTable.java
│   │   ├── Reservation.java
│   │   ├── Order.java
│   │   ├── OrderDetail.java
│   │   ├── ItemRating.java
│   │   ├── Notification.java
│   │   ├── NotificationType.java
│   │   ├── Payment.java
│   │   └── PaymentMethod.java
│   │
│   ├── database
│   │   ├── AppDatabase.java
│   │   ├── UserDao.java
│   │   ├── RoleDao.java
│   │   ├── CategoryDao.java
│   │   ├── MenuItemDao.java
│   │   ├── DiningTableDao.java
│   │   ├── ReservationDao.java
│   │   ├── OrderDao.java
│   │   ├── OrderDetailDao.java
│   │   ├── ItemRatingDao.java
│   │   ├── NotificationDao.java
│   │   ├── PaymentDao.java
│   │   └── PaymentMethodDao.java
│   │
│   └── repository
│       ├── AuthRepository.java
│       ├── MenuRepository.java
│       ├── OrderRepository.java
│       ├── ReservationRepository.java
│       ├── PaymentRepository.java
│       └── NotificationRepository.java
│
├── ui
│   ├── auth
│   │   ├── LoginActivity.java
│   │   └── RegisterActivity.java
│   │
│   ├── customer
│   │   ├── home
│   │   │   └── CustomerHomeActivity.java
│   │   │
│   │   ├── menu
│   │   │   ├── MenuFragment.java
│   │   │   └── MenuAdapter.java
│   │   │
│   │   ├── cart
│   │   │   ├── CartFragment.java
│   │   │   └── CartAdapter.java
│   │   │
│   │   ├── order
│   │   │   ├── OrderHistoryFragment.java
│   │   │   └── OrderHistoryAdapter.java
│   │   │
│   │   └── reservation
│   │       └── ReservationFragment.java
│   │
│   ├── staff
│   │   ├── home
│   │   │   └── StaffHomeActivity.java
│   │   │
│   │   ├── order
│   │   │   ├── OrderManageFragment.java
│   │   │   └── OrderManageAdapter.java
│   │   │
│   │   └── table
│   │       └── TableStatusFragment.java
│   │
│   └── owner
│       ├── home
│       │   └── OwnerHomeActivity.java
│       │
│       ├── menu
│       │   ├── ManageMenuFragment.java
│       │   └── EditMenuItemActivity.java
│       │
│       ├── staff
│       │   └── StaffManageFragment.java
│       │
│       └── report
│           └── RevenueFragment.java
│
└── MyApplication.java
