# 🎮 Steam Game Market Segmentation using K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458)
![Status](https://img.shields.io/badge/Status-Completed-success)

> **Proyek Ujian Akhir Semester (UAS)** > **Mata Kuliah:** Big Data & Data Mining  
> **Dosen Pengampu:** Anna Baita, S.Kom., M.Kom.

---

## 👨‍💻 Author
* **Nama:** Izzuddin Akmal daffani Ramadhan
* **NIM:** 23.11.5483
* **Kelas:** 23S1IF-BigData2(ST168)

---

## 📖 Project Overview
Proyek ini bertujuan untuk melakukan **segmentasi pasar industri game** menggunakan dataset dari platform Steam. Dengan menerapkan algoritma *Unsupervised Learning* (**K-Means Clustering**), sistem ini mengelompokkan lebih dari 120.000 judul game ke dalam kategori bisnis yang distingtif berdasarkan pola harga, sentimen ulasan, dan keterlibatan pemain (*playtime*).

Tujuan utama proyek ini adalah membantu developer dan analis pasar memahami karakteristik game yang sukses ("Blockbuster") dibandingkan dengan game standar (*Niche*).

### 🔍 Key Methodology
1.  **Data Preprocessing:** Pembersihan *missing values* dan seleksi fitur numerik esensial.
2.  **Feature Engineering:** Pembuatan fitur baru `Sentiment_Ratio` untuk menormalisasi bias jumlah ulasan.
3.  **Outlier Handling:** Menggunakan **Robust Scaler** untuk menangani distribusi data Steam yang sangat timpang (*skewed*) dan penuh *outliers* ekstrem.
4.  **Modeling:** Menggunakan algoritma **K-Means** dengan inisialisasi `k-means++`.
5.  **Optimization:** Penentuan jumlah klaster optimal ($k=4$) menggunakan **Elbow Method**.

---

## 📊 Analysis Results
Berdasarkan evaluasi model, terbentuk 4 klaster pasar dengan karakteristik sebagai berikut:

| Cluster | Label Bisnis | Karakteristik Utama |
| :--- | :--- | :--- |
| **0** | *The Silent Majority* | Game standar/indie, harga menengah (~$18), ulasan rendah. Mayoritas populasi. |
| **1** | *Premium Blockbusters* | Game AAA berbayar mahal (~$36), kualitas kritik tinggi, ulasan masif. |
| **2** | *Engagement Monsters* | Game Gratis (F2P), ulasan sedikit tapi **Playtime Ekstrem** (Jutaan menit). Anomali unik. |
| **3** | *Viral Hits* | Game Gratis/Murah dengan popularitas ulasan tertinggi (Jutaan reviews). |

### 📈 Model Evaluation
Model mencapai performa separasi yang sangat tinggi dikarenakan karakteristik data yang mengikuti distribusi *Power Law*:
* **Silhouette Score:** `0.9981` (Sangat Baik)
* **Davies-Bouldin Index:** `0.1777` (Sangat Baik)

---

## 🛠️ Tech Stack & Libraries
Proyek ini dikerjakan menggunakan **Google Colab** dengan library Python:
* `pandas` & `numpy`: Manipulasi data.
* `matplotlib` & `seaborn`: Visualisasi data (Heatmap, Histogram, Scatter Plot).
* `scikit-learn`: Pembuatan model K-Means, PCA, dan Evaluasi Metrik.
* `joblib`: Penyimpanan model (Model Persistence).
* `opendatasets`: Pengambilan data langsung dari Kaggle.

---

## 📂 File Structure
Penjelasan singkat mengenai file yang ada di repositori ini:

* `UAS_BDDM_23_11_5483_Izzuddin_A_D_R.ipynb`: Source code utama (Jupyter Notebook) berisi seluruh proses dari EDA hingga Modeling.
* `kmeans_steam_model.pkl`: File model K-Means yang sudah dilatih dan siap digunakan.
* `robust_scaler_steam.pkl`: File scaler untuk normalisasi data input baru (Wajib digunakan bersamaan dengan model).
* `games.csv`: Dataset mentah (jika diupload) atau bisa diunduh via script.

---

## 🚀 How to Run
1.  **Clone Repository**
    ```bash
    git clone [https://github.com/username/nama-repo-anda.git](https://github.com/username/nama-repo-anda.git)
    ```
2.  **Install Dependencies**
    Pastikan library berikut terinstall:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn opendatasets joblib
    ```
3.  **Run Notebook**
    Buka file `.ipynb` menggunakan Jupyter Notebook, VS Code, atau Google Colab.

---

## 🔗 Dataset Source
Dataset yang digunakan berasal dari Kaggle:
* **Title:** Steam Store Games (Clean dataset)
* **Link:** [Kaggle Dataset URL](https://www.kaggle.com/datasets/nikdavis/steam-store-games)

---

<center>
Created for Final Exam Assignment • 2026
</center>
