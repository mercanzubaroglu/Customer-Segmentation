#  Customer Segmentation with K-Means Clustering

This project uses unsupervised machine learning to segment customers based on their demographic features and spending behaviors.  
Bu proje, müşterileri yaş, gelir ve harcama alışkanlıklarına göre gruplandırmak amacıyla K-Means algoritmasıyla müşteri segmentasyonu yapar.

---

## 📁 Dataset Information

- **Dataset Name:** Customer Personality Analysis  
- **Source:** [Kaggle - Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
- **Size:** 2240 records, 29 features  
- **Delimiter:** Tab-separated (.csv with `\t`)

---

## 🔧 Techniques Used / Kullanılan Yöntemler

- 🧹 Data Cleaning & Feature Engineering (Age, TotalSpending, TotalChildren)
- ⚖️ Feature Scaling with StandardScaler
- 📉 Dimensionality Reduction using PCA (2 Components)
- 📊 Customer Segmentation via **K-Means Clustering**
- 📌 Optimal K found via Elbow & Silhouette Methods
- 📈 Data Visualization with **Seaborn** & **Matplotlib**

---

## 🧪 Visualizations / Görselleştirmeler

| Visualization | Description |
|---------------|-------------|
| 📊 `Income Distribution / Gelir Dağılımı` | Müşterilerin gelir dağılımını gösterir (Histogram + KDE) |
| 📉 `PCA Visualization / PCA Görselleştirmesi` | 2 boyuta indirgenmiş müşteri verisi üzerinde küme dağılımı |
| 🔢 `Number of Clusters / Küme Sayısı` | Elbow method ile en uygun K değeri seçimi |
| 🧭 `Customer Segmentation / Müşteri Segmentasyonu` | PCA düzleminde kümelenmiş müşteri grupları (KMeans) |
| 🧍 `Customer Count per Cluster / Her Kümede Kaç Müşteri Var?` | Her segmentteki müşteri sayısını gösterir |
| 💸 `Average Income by Cluster / Küme Bazlı Ortalama Gelir` | Segmentlere göre ortalama gelir kıyaslaması |
| 👨‍👩‍👧‍👦 `Children vs Spending / Çocuk Sayısı - Harcama İlişkisi` | Çocuk sayısına göre toplam harcama eğilimi |
| 🔥 `Cluster Spending Heatmap / Küme Harcama Isı Haritası` | Segment bazında ürün kategorisi harcama karşılaştırması |

---

## 📖 Methodology (Yöntem Açıklamaları)

### 🔍 Why PCA (Principal Component Analysis)?

PCA is used to reduce the dimensionality of the dataset while retaining most of the variance. This not only helps in faster computation but also improves visual interpretability.

🧬 PCA (Ana Bileşen Analizi), yüksek boyutlu verileri daha az boyuta indirerek görsel analiz ve model performansını iyileştirir.

In our case, reducing to 2 dimensions allowed us to:
- Visualize clusters clearly
- Apply KMeans faster
- Avoid noise and redundancy in features

---

### 📉 Why Elbow Method?

The Elbow Method is a widely used technique for finding the optimal number of clusters (K) in unsupervised learning tasks like K-Means.

In this project, we apply the Elbow Method by plotting the Sum of Squared Errors (SSE) for a range of K values. The 'elbow point' on the curve—where the rate of decrease sharply slows—indicates the most appropriate number of clusters.

🧠 Dirsek Yöntemi, K-means algoritmasında optimum küme sayısını (K) belirlemek için kullanılan klasik bir yöntemdir. Farklı K değerleri için toplam hata kareleri (SSE) hesaplanır ve grafik üzerindeki kırılma noktası optimal K'yı verir.

Bu projede K = 4 için belirgin bir kırılma gözlenmiştir.

---

### 🧠 Why KMeans?

KMeans is a centroid-based, unsupervised clustering algorithm that is efficient, interpretable, and widely used for segmentation problems.

We selected KMeans because:
- It handles large datasets well
- Results are easy to interpret (centroids and labels)
- It aligns well with PCA-transformed continuous data

Kısacası, müşteri segmentasyonu gibi görevlerde KMeans genellikle ilk tercihtir çünkü:
- Hızlı çalışır
- Yorumlaması kolaydır
- Sürekli değişkenlerle uyumludur

---
 

