Proyek ini bertujuan untuk mengklasifikasikan siswa yang lulus atau tidak lulus berdasarkan nilai matematika, membaca, dan menulis, menggunakan Decision Tree Classifier dari scikit-learn.

Dataset yang digunakan adalah StudentsPerformance.csv dari Kaggle. Prediksi dilakukan dengan membuat label baru bernama lulus berdasarkan rata-rata nilai >= 60.

Struktur Program dan Penjelasan

Import Library Digunakan untuk memuat pustaka yang dibutuhkan:
pandas: untuk mengelola data tabular
matplotlib: untuk membuat visualisasi
sklearn.model_selection: untuk membagi data
sklearn.tree: untuk membangun dan menggambar decision tree
sklearn.metrics: untuk evaluasi model (akurasi, precision, recall, f1-score)

Load dan Intip Dataset:
Membaca dataset StudentsPerformance.csv dan menampilkan 5 baris awal menggunakan df.head() untuk memastikan struktur kolom sesuai harapan.

Persiapan Data:
Menghitung kolom rata_rata dari 3 nilai ujian.
Menambahkan kolom lulus dengan kriteria: jika rata_rata >= 60 maka dianggap lulus (1), jika tidak (0).
Menentukan X (fitur) dan y (label).

Split Data Membagi data menjadi:
data latih (X_train, y_train)
data uji (X_test, y_test)

Training Model:
Menggunakan DecisionTreeClassifier() untuk melatih model pada data latih.

Evaluasi Model:
Melakukan prediksi terhadap X_test.
Mengukur akurasi dengan accuracy_score().
Menampilkan metrik klasifikasi dengan classification_report().

Visualisasi:
Menggunakan plot_tree() untuk menggambar struktur pohon keputusan yang telah dilatih.


Singkatan Umum dalam Kode:
df: DataFrame (struktur data tabular)
X: Fitur input (nilai ujian siswa)
y: Label output (1 = lulus, 0 = tidak lulus)
X_train: Data latih (fitur)
X_test: Data uji (fitur)
y_train: Data latih (label)
y_test: Data uji (label)
y_pred: Hasil prediksi oleh model


Sumber Dataset
Kaggle: https://www.kaggle.com/datasets/spscientist/students-performance-in-exams 
