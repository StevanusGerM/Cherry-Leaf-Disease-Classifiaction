🍒 Cherry Leaf Disease Detection

Proyek computer vision untuk mengklasifikasikan penyakit daun ceri menggunakan TensorFlow/Keras.

📂 Struktur & Pembagian Dataset

Total Data: 2.547 gambar (5 kelas).

Pembagian Data: 70% Train, 15% Validation, 15% Test (mencegah data leakage, menggunakan seed 1234).

Distribusi Kelas:

Cherry Leaf Scorch: 770 gambar

Cherry purple leaf spot: 690 gambar

Cherry brown_spot: 429 gambar

Cherry Normal leaf: 350 gambar

Cherry shot hole disease: 308 gambar

Preprocessing: Ukuran gambar diubah dari 800x1000 piksel menjadi 224x224 piksel.

🛠️ Dependencies

pip install tensorflow scikit-learn pillow matplotlib seaborn numpy


🚀 Quick Start

import tensorflow as tf

train_ds = tf.keras.utils.image_dataset_from_directory(
    'path/to/train',
    seed=1234,
    image_size=(224, 224),
    batch_size=32,
    label_mode='categorical'
)
