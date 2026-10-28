# 🔳 QR Code Generation using Python

A beginner-friendly Python project that generates **Website QR Codes** and **UPI Payment QR Codes** using the `qrcode` library. Users can create QR codes for URLs, UPI IDs, and payment requests with an amount, and save them as PNG images.

## ✨ Features

- 🌐 Generate QR codes for website URLs.
- 🔗 Validate URLs before generating QR codes.
- 💳 Generate UPI Payment QR codes.
- 💰 Add payment amount to UPI QR codes.
- 👤 Include payee name in UPI QR codes.
- 💾 Save QR codes as PNG images.
- 🖥️ Simple console-based interface for beginners.

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Core programming language |
| qrcode | QR code generation |
| Pillow | Image creation (dependency of qrcode) |
| Jupyter Notebook | Development environment |

## 📁 Project Structure

```text
QR-Code-Generation/
│
├── QR Code Generation.ipynb   # Main project notebook
├── FirstQR_2026.png           # Website QR output
├── UPI_QR.png                 # UPI QR output
└── README.md                  # Project documentation
```

*The output images are generated automatically when the notebook is executed.*

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/QR-Code-Generation.git
cd QR-Code-Generation
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Install the required library

```bash
pip install qrcode[pil]
```

### 3. Run the notebook

```bash
jupyter notebook
```

Open **`QR Code Generation.ipynb`** and run the cells in order.

## 🚀 How to Use

### Website QR Generator

1. Run the Website QR cell.
2. Enter a valid URL.
3. The QR code will be generated and saved as:

```text
FirstQR_2026.png
```

### UPI Payment QR Generator

1. Run the UPI QR cell.
2. Enter:
   - UPI ID
   - Payee Name
   - Payment Amount
3. The notebook creates a UPI payment QR code that can be scanned by compatible UPI apps.

Example UPI format:

```text
upi://pay?pa=name@bank&pn=John&am=100
```

## 📸 Output

The project generates PNG QR code images like:

- `FirstQR_2026.png` – Website QR
- `UPI_QR.png` – UPI Payment QR

These images can be scanned using any compatible QR scanner or UPI application.

## 📌 Project Highlights

- Beginner-friendly Python project.
- Input validation for website URLs.
- Dynamic QR code generation.
- UPI payment QR creation with amount support.
- Lightweight and easy to understand.

## 🔮 Future Improvements

- 🎨 Custom QR colors and styles.
- 🖼️ Add logos inside QR codes.
- 📱 Generate Wi-Fi QR codes.
- 📧 Generate Email and Contact QR codes.
- 🌐 Build a Flask web interface.
- 📂 Batch QR code generation from CSV.


---

⭐ If you found this project useful, don't forget to **Star** the repository!
