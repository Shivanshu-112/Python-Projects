# 🖼️ Text to Image Converter using Python

A simple Python project that converts user-entered text into an image using the **Pillow (PIL)** library. The program automatically wraps long text into multiple lines, renders it in red on a white background, and saves the generated image as a PNG file.

## ✨ Features

- 📝 **User Input** — Enter any text through the console.
- 🖼️ **Image Generation** — Convert text into an image.
- ↔️ **Automatic Text Wrapping** — Fit long text within the available image width.
- 🎨 **Text Styling** — Display text in red on a white background.
- 💾 **PNG Export** — Save the generated image as `test_sample_24.png`.
- 📐 **Fixed Image Dimensions** — Generate images with a resolution of 800 × 300 pixels.

## 🛠️ Tech Stack

- **Python** — Core programming language
- **Pillow (PIL)** — Image creation, drawing, and text rendering

## 📁 Project Structure

```text
Text-to-Image/
│
├── image to text.ipynb   # Jupyter Notebook source code
├── test_sample_24.png    # Generated output image
└── README.md             # Project documentation
```

*Note: The PNG image is generated when you run the notebook. It may not exist in the repository until you add it.*

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Text-to-Image.git
cd Text-to-Image
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Install the required library

```bash
pip install Pillow
```

### 3. Run the notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `image to text.ipynb` and run the second code cell.

## 🚀 How It Works

1. The program asks the user to enter text.
2. It creates a blank white image of size 800 × 300 pixels.
3. It loads the default Pillow font.
4. It measures the width of each line and wraps words when the available width is exceeded.
5. It draws the wrapped text in red, starting at a left margin of 50 pixels.
6. It saves the final image as `test_sample_24.png`.

## 💻 Code

```python
from PIL import Image, ImageDraw, ImageFont

text = input("Enter your text: ")

image = Image.new("RGB", (800, 300), "white")
draw = ImageDraw.Draw(image)
font = ImageFont.load_default()

left_margin = 50
right_margin = 50
available_width = 800 - left_margin - right_margin

wrapped_lines = []
current_line = ""

for word in text.split():
    test_line = f"{current_line} {word}".strip()
    text_width = draw.textbbox((0, 0), test_line, font=font)[2]

    if text_width <= available_width:
        current_line = test_line
    else:
        if current_line:
            wrapped_lines.append(current_line)
        current_line = word

if current_line:
    wrapped_lines.append(current_line)

y = 50
for line in wrapped_lines:
    draw.text((left_margin, y), line, fill="red", font=font)
    y += 25

image.save("test_sample_24.png")
print("Image generated successfully!")
```

## 📷 Output

The generated image has the following properties:

| Property | Value |
|---|---|
| Image size | 800 × 300 pixels |
| Background | White |
| Text color | Red |
| Font | Pillow default font |
| Output format | PNG |
| Output filename | `test_sample_24.png` |

## 🔮 Future Improvements

- 🎨 Add custom font styles and colors.
- 📏 Allow users to choose image dimensions.
- 🖼️ Add background colors and images.
- 🔠 Support adjustable font sizes.
- 💾 Allow users to choose the output filename.
- 🌐 Build a web interface for text-to-image conversion.


---

⭐ If you find this project useful, consider giving the repository a star!

*Built with Python and Pillow.*
