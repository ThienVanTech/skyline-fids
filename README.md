# SkyLine FIDS - Hệ thống Hiển thị Thông tin Chuyến bay

> A modern, affordable, and intuitive Flight Information Display System designed to enhance passenger experience and optimize operations at smaller airports.

[English](#english) | [Tiếng Việt](#tiếng-việt)

---

## Tiếng Việt

### 📋 Giới thiệu

SkyLine FIDS là một hệ thống hiển thị thông tin chuyến bay hiện đại, được xây dựng bằng Next.js và React. Hệ thống cung cấp giao diện trực quan để hiển thị thông tin chuyến bay theo thời gian thực cho các sân bay nhỏ và vừa.

### ✨ Tính năng chính

- 🛫 Bảng thông tin chuyến bay khởi hành (Departures Board)
- 🛬 Bảng thông tin chuyến bay đến (Arrivals Board)
- ✅ Màn hình làm thủ tục (Check-in Display)
- 🚪 Hiển thị thông tin cổng lên máy bay (Boarding Gate Display)
- 🧳 Thông tin hành lý (Baggage Information)
- 📍 Thông tin chi tiết cổng (Gate Information)
- 🌓 Hỗ trợ chế độ sáng/tối
- 📱 Giao diện responsive cho mọi thiết bị

### 🔧 Yêu cầu hệ thống

Trước khi bắt đầu, hãy đảm bảo máy tính của bạn đã cài đặt:

- **Node.js**: phiên bản 18.x hoặc cao hơn (khuyến nghị 20.x)
- **npm**: phiên bản 9.x hoặc cao hơn
- **Git**: để clone repository

### 📥 Cài đặt

#### Bước 1: Clone repository

```bash
git clone https://github.com/ThienVanTech/skyline-fids.git
cd skyline-fids
```

#### Bước 2: Cài đặt dependencies

```bash
npm install
```

Lệnh này sẽ cài đặt tất cả các package cần thiết được liệt kê trong `package.json`.

### 🚀 Chạy ứng dụng

#### Chế độ Development (Phát triển)

Để chạy ứng dụng ở chế độ development với hot-reload:

```bash
npm run dev
```

Sau khi chạy lệnh, mở trình duyệt và truy cập:
- **URL**: http://localhost:3000

Ứng dụng sẽ tự động reload khi bạn chỉnh sửa code.

#### Build cho Production

Để build ứng dụng cho môi trường production:

```bash
npm run build
```

Lệnh này sẽ tạo ra thư mục `out/` chứa các file tĩnh đã được tối ưu hóa.

#### Chạy bản Production

Sau khi build, bạn có thể chạy ứng dụng ở chế độ production:

```bash
npm run start
```

**Lưu ý**: Vì project được cấu hình với `output: 'export'`, bạn có thể deploy các file trong thư mục `out/` lên bất kỳ hosting tĩnh nào (Netlify, Vercel, GitHub Pages, v.v.).

### 🧪 Kiểm tra code

Để chạy ESLint và kiểm tra lỗi code:

```bash
npm run lint
```

### 📁 Cấu trúc thư mục

```
skyline-fids/
├── app/                    # Next.js App Router
│   ├── examples/          # Trang ví dụ các màn hình FIDS
│   ├── pricing/           # Trang giá
│   ├── resources/         # Trang tài nguyên
│   ├── globals.css        # Styles toàn cục
│   ├── layout.tsx         # Layout chính
│   └── page.tsx           # Trang chủ
├── components/            # React components
│   ├── examples/         # Components cho các màn hình FIDS
│   ├── ui/               # UI components (shadcn/ui)
│   ├── Navbar.tsx        # Component điều hướng
│   ├── Footer.tsx        # Component footer
│   └── ...               # Các components khác
├── lib/                  # Utility functions
├── hooks/                # Custom React hooks
├── public/               # Static files (images, fonts, etc.)
├── next.config.js        # Cấu hình Next.js
├── tailwind.config.ts    # Cấu hình Tailwind CSS
├── tsconfig.json         # Cấu hình TypeScript
└── package.json          # Dependencies và scripts

```

### 🎨 Công nghệ sử dụng

- **Framework**: [Next.js 13.5.1](https://nextjs.org/) (App Router)
- **UI Library**: [React 18.2.0](https://react.dev/)
- **Language**: [TypeScript 5.2.2](https://www.typescriptlang.org/)
- **Styling**: [Tailwind CSS 3.3.3](https://tailwindcss.com/)
- **UI Components**: [Radix UI](https://www.radix-ui.com/)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Animations**: Tailwind CSS Animate
- **Theme**: next-themes (hỗ trợ dark mode)

### 🔍 Các trang chính

- **Trang chủ** (`/`): Giới thiệu về SkyLine FIDS với các tính năng và lợi ích
- **Examples** (`/examples`): Demo các loại màn hình FIDS khác nhau
- **Pricing** (`/pricing`): Thông tin về giá và gói dịch vụ
- **Resources** (`/resources`): Tài nguyên và tài liệu hỗ trợ
- **Thank You** (`/thank-you`): Trang cảm ơn sau khi đăng ký

### 🛠️ Customization

#### Thay đổi màu sắc chủ đạo

Chỉnh sửa file `tailwind.config.ts` để thay đổi theme colors:

```typescript
theme: {
  extend: {
    colors: {
      // Thêm hoặc chỉnh sửa màu sắc tại đây
    }
  }
}
```

#### Thêm màn hình FIDS mới

1. Tạo component mới trong `components/examples/`
2. Import và thêm vào `app/examples/page.tsx`
3. Thêm vào mảng `displays` với icon và mô tả tương ứng

### ⚠️ Troubleshooting

#### Lỗi "Module not found"

```bash
# Xóa node_modules và cài đặt lại
rm -rf node_modules package-lock.json
npm install
```

#### Lỗi khi build

```bash
# Xóa cache Next.js
rm -rf .next
npm run build
```

#### Port 3000 đã được sử dụng

```bash
# Chạy trên port khác
PORT=3001 npm run dev
```

### 📝 Scripts có sẵn

| Script | Mô tả |
|--------|-------|
| `npm run dev` | Chạy development server |
| `npm run build` | Build ứng dụng cho production |
| `npm run start` | Chạy production server |
| `npm run lint` | Kiểm tra lỗi với ESLint |

### 🤝 Đóng góp

Nếu bạn muốn đóng góp cho project:

1. Fork repository
2. Tạo branch mới (`git checkout -b feature/TinhNangMoi`)
3. Commit thay đổi (`git commit -m 'Thêm tính năng mới'`)
4. Push lên branch (`git push origin feature/TinhNangMoi`)
5. Tạo Pull Request

### 📄 License

Copyright © 2024 ThienVanTech. All rights reserved.

### 📞 Liên hệ

Nếu có bất kỳ câu hỏi nào, vui lòng tạo issue trên [GitHub Issues](https://github.com/ThienVanTech/skyline-fids/issues).

---

## English

### 📋 Introduction

SkyLine FIDS is a modern Flight Information Display System built with Next.js and React. The system provides an intuitive interface to display real-time flight information for small to medium-sized airports.

### ✨ Key Features

- 🛫 Departures Board
- 🛬 Arrivals Board
- ✅ Check-in Display
- 🚪 Boarding Gate Display
- 🧳 Baggage Information
- 📍 Gate Information
- 🌓 Light/Dark mode support
- 📱 Responsive design for all devices

### 🔧 System Requirements

Before you begin, ensure you have installed:

- **Node.js**: version 18.x or higher (20.x recommended)
- **npm**: version 9.x or higher
- **Git**: to clone the repository

### 📥 Installation

#### Step 1: Clone the repository

```bash
git clone https://github.com/ThienVanTech/skyline-fids.git
cd skyline-fids
```

#### Step 2: Install dependencies

```bash
npm install
```

This command will install all required packages listed in `package.json`.

### 🚀 Running the Application

#### Development Mode

To run the application in development mode with hot-reload:

```bash
npm run dev
```

After running the command, open your browser and visit:
- **URL**: http://localhost:3000

The application will automatically reload when you edit the code.

#### Build for Production

To build the application for production:

```bash
npm run build
```

This command will create an `out/` directory containing optimized static files.

#### Run Production Build

After building, you can run the application in production mode:

```bash
npm run start
```

**Note**: Since the project is configured with `output: 'export'`, you can deploy the files in the `out/` directory to any static hosting service (Netlify, Vercel, GitHub Pages, etc.).

### 🧪 Code Linting

To run ESLint and check for code errors:

```bash
npm run lint
```

### 📁 Project Structure

```
skyline-fids/
├── app/                    # Next.js App Router
│   ├── examples/          # FIDS display examples page
│   ├── pricing/           # Pricing page
│   ├── resources/         # Resources page
│   ├── globals.css        # Global styles
│   ├── layout.tsx         # Main layout
│   └── page.tsx           # Home page
├── components/            # React components
│   ├── examples/         # FIDS display components
│   ├── ui/               # UI components (shadcn/ui)
│   ├── Navbar.tsx        # Navigation component
│   ├── Footer.tsx        # Footer component
│   └── ...               # Other components
├── lib/                  # Utility functions
├── hooks/                # Custom React hooks
├── public/               # Static files (images, fonts, etc.)
├── next.config.js        # Next.js configuration
├── tailwind.config.ts    # Tailwind CSS configuration
├── tsconfig.json         # TypeScript configuration
└── package.json          # Dependencies and scripts
```

### 🎨 Tech Stack

- **Framework**: [Next.js 13.5.1](https://nextjs.org/) (App Router)
- **UI Library**: [React 18.2.0](https://react.dev/)
- **Language**: [TypeScript 5.2.2](https://www.typescriptlang.org/)
- **Styling**: [Tailwind CSS 3.3.3](https://tailwindcss.com/)
- **UI Components**: [Radix UI](https://www.radix-ui.com/)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Animations**: Tailwind CSS Animate
- **Theme**: next-themes (dark mode support)

### 🔍 Main Pages

- **Home** (`/`): Introduction to SkyLine FIDS with features and benefits
- **Examples** (`/examples`): Demo of different FIDS display types
- **Pricing** (`/pricing`): Pricing information and service packages
- **Resources** (`/resources`): Support resources and documentation
- **Thank You** (`/thank-you`): Thank you page after registration

### 🛠️ Customization

#### Change Theme Colors

Edit `tailwind.config.ts` to change theme colors:

```typescript
theme: {
  extend: {
    colors: {
      // Add or modify colors here
    }
  }
}
```

#### Add New FIDS Display

1. Create a new component in `components/examples/`
2. Import and add to `app/examples/page.tsx`
3. Add to the `displays` array with corresponding icon and description

### ⚠️ Troubleshooting

#### "Module not found" Error

```bash
# Remove node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

#### Build Error

```bash
# Clear Next.js cache
rm -rf .next
npm run build
```

#### Port 3000 Already in Use

```bash
# Run on a different port
PORT=3001 npm run dev
```

### 📝 Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Run development server |
| `npm run build` | Build application for production |
| `npm run start` | Run production server |
| `npm run lint` | Check errors with ESLint |

### 🤝 Contributing

If you want to contribute to the project:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/NewFeature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/NewFeature`)
5. Create a Pull Request

### 📄 License

Copyright © 2024 ThienVanTech. All rights reserved.

### 📞 Contact

For any questions, please create an issue on [GitHub Issues](https://github.com/ThienVanTech/skyline-fids/issues).

---

**Made with ❤️ by ThienVanTech**
