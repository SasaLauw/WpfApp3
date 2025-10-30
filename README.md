Week 08 (2025/10/30)

✨RenderTargetBitmap 可以將一個 Visual 或其子類別的元素（例如 Canvas 元件）渲染成一個位圖影像，然後您就可以將這個位圖保存為圖形檔案（如 PNG、JPEG等）。
✨PixelFormats 是 WPF 影像處理中一個靜態類別1它位於 System.Windows.Media 命名空間。它提供了一系列預定義的像素格式（PixelFormat），用於指定位圖影像中每個像素的資料結構和顏色深度。
✨將 RenderTargetBitmap 存檔通常需要以下三個核心物件：
1. RenderTargetBitmap：已經渲染好的來源位圖（bitmap）。
2. BitmapEncoder：決定最終的檔案格式（例如 PngBitmapEncoder）*
3. FileStream：用於將編碼後的數據寫入磁碟。
✨BitmapEncoder（位於 System. Windows Media.Imaging 命名空間）是 WPF 影像處理
中的抽象基類。它的核心功能是：
將一個或多個 BitmapFrame 物件（包含位圖數據和元數據）轉換為標準的檔案格式（例如 PNG、JPEG 等）的二進制數據流，並將其寫入 Stream中。
