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
✨using （Filestream fs=・.）（Using 語句與資源管理）
📌using 語句：這是C# 中一個非常重要的結構，用於確保實現了 IDisposable 介面的物件在使用完畢後，無論程式碼區塊是否正常結束（即使發生例外），都會自動且可靠地呼叫其 Dispose（）方法。
FileStream：這是一個用於讀取或寫入檔案的類別。檔案串流是一種非託管資源(Unmanaged Resource)
📌需要明確釋放，否則可能會導致檔被鎖定或資源洩漏。
📌fs：這是我們為這個 FileStream實例取的變數名稱。
📌newFileStream(saveFileDiolog.FileName,FileMode.Create）：這是 FileStream 的建構函式，用於建立檔案串流或創建一個新檔案，當 using
區塊結束時，fs 會被自動關閉和釋放。
✨pngEncoder.Save（fs）；（執行圖像編碼和寫入）
📌pngEncoder：這是程式碼中前面已建立的一個 PngBitmapEncoder 實例（繼承自
Bi tmapEncoder ）。此編碼器已經準備好了要儲存的圖像數據（通常已將 BitmapFrome加入其中。
