# 📂 Google Drive Shared Folder Cloner

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ciwga/Google-Drive-Shared-Folder-Cloner/blob/main/GDrive_Shared_Folder_Cloner.ipynb)

A powerful Google Colab notebook designed to clone/copy folders shared with you directly to your own "My Drive" without downloading them to your local machine first.

## 🌟 Why use this?

Usually, copying large shared folders in Google Drive is tricky. You often have to download them to your PC and re-upload them, consuming bandwidth and time. **This tool runs entirely on Google's servers.**

### Key Features
* **🚀 Server-Side Copy:** No local bandwidth usage.
* **📦 Large File Support:** Uses chunk-based copying (1MB buffer) to prevent memory overflows and timeouts on huge files (tested with 15GB+ files).
* **📊 Visual Progress:** Includes a real-time progress bar (`tqdm`) showing data transfer speed and ETA.
* **🖥️ GUI Selector:** Uses `ipyfilechooser` for easy folder selection (no need to manually type paths).
* **ownership:** The copied files become **yours**, meaning you have full control even if the original owner deletes them.

---

## ⚠️ Prerequisite: The "Shortcut" Trick

Google Colab cannot directly access the **"Shared with me"** tab. You must create a bridge first:

1.  Go to Google Drive and open **"Shared with me"**.
2.  Right-click the folder you want to copy.
3.  Select **Organize** $\rightarrow$ **Add shortcut**.
4.  Choose **"My Drive"** as the destination and click **Add**.

*Now, the script will be able to see the shared folder inside your Drive.*

---

## 🛠️ How to Use

1.  Click the **"Open in Colab"** badge above.
2.  **Step 1:** Run the setup cell to mount your Google Drive and install the UI library.
3.  **Step 2:** Use the file selector to pick:
    * **Source:** The shortcut you just created.
    * **Target:** Where you want the *real* copy to be saved.
4.  **Step 3:** Run the execution cell and wait for the progress bar to finish.

## 📦 Libraries Used
* `shutil`: For high-level file operations.
* `ipyfilechooser`: For the folder selection GUI.
* `tqdm`: For the progress bar.

## 📝 License
This project is open-source. Feel free to modify and improve.
