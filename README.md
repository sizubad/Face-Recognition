# UAS Deep Learning :robot:
# Nama Kelompok :wave:
| Nama                       | NPM       |
| ----------------------     | :--------:|
| Siti Zubaidah              | G1A021002 | 
| Mareta Aliana	             | G1A021038 |
| Rizky Putri Pratiwi        | G1A021044 | 

# Latar Belakang :brain:

Pembelajaran daring di Universitas Bengkulu khususnya di Prodi Teknik Informatika sering menghadapi kendala, seperti rendahnya tingkat partisipasi mahasiswa dan adanya praktik tidak jujur, seperti meminta orang 
lain menggantikan kehadiran mereka. Untuk mengatasi tantangan tersebut, kami merancang sistem berbasis deep learning menggunakan teknologi *face recognition* dengan arsitektur 
**MobileNet V2**. Sistem ini bertujuan membantu dosen memastikan mahasiswa yang hadir adalah peserta sebenarnya, bukan pihak lain. Teknologi MobileNet V2 dipilih karena mampu 
memberikan hasil akurasi yang tinggi dengan kebutuhan komputasi yang efisien. Diharapkan, solusi ini dapat meningkatkan kejujuran dan efektivitas proses pembelajaran daring
di lingkungan Universitas Bengkulu.
# Dataset :floppy_disk:
Dataset yang kami gunakan berupa sampel dari 5 orang mahasiswa dengan masing-masing 150 foto dengan total 750 data yang kemudian diugmentasi secara realtime dengan.<br/>

    rotation_range=20,
    zoom_range=0.15,
    width_shift_range=0.2,
    height_shift_range=0.2,
    shear_range=0.15,
    horizontal_flip=True,
    fill_mode="nearest"
# Hasil dan Pembahasan :clipboard:
## Matriks Evaluasi :blue_book:
![Overview Banner!](https://github.com/sizubad/Face-Recognition/blob/ffe6de8ac32ce737b056bbbecf940447b53f5867/Matriks%20Evaluasi.png)<br/>
Berdasarkan laporan evaluasi model klasifikasi, performa model menunjukkan **akurasi keseluruhan sebesar 87%**. Hal ini mengindikasikan bahwa sebagian besar prediksi yang
dilakukan oleh model sudah benar. Namun, terdapat variasi performa antar kelas. Misalnya, kelas "Mareta Aliana" memiliki precision 82% dan recall 90%, yang berarti model 
cukup baik mengenali kelas ini, meskipun masih terdapat beberapa prediksi salah. Di sisi lain, kelas "Nanda Nurahmanita Putri" memiliki recall yang lebih rendah, yaitu 63%, 
menunjukkan bahwa model sering gagal mendeteksi sampel dari kelas ini. Sebaliknya, kelas "Rizky Putri Pratiwi" menunjukkan performa sempurna dengan nilai precision, recall, 
dan f1-score sebesar 1.00, artinya model mampu mengenali semua sampel dari kelas ini dengan benar. Secara keseluruhan, nilai rata-rata precision, recall, dan f1-score
menunjukkan hasil yang cukup seimbang, masing-masing sebesar 88%, 87%, dan 87%, baik dalam macro average maupun weighted average. <br />

## Grafik Evaluasi Model :chart_with_upwards_trend:
### Grafik Training dan Validation Accuracy
![Overview Banner!](https://github.com/sizubad/Face-Recognition/blob/ffe6de8ac32ce737b056bbbecf940447b53f5867/Accuracy.png)<br/>
### Grafik Training dan Validation Loss
![Overview Banner!](https://github.com/sizubad/Face-Recognition/blob/ffe6de8ac32ce737b056bbbecf940447b53f5867/Loss.png)<br/>
Berdasarkan kedua grafik evaluasi model, yaitu Training and Validation Accuracy dan Training and Validation Loss, dapat disimpulkan bahwa model menunjukkan kinerja yang
cukup baik selama pelatihan. Akurasi pelatihan meningkat secara konsisten, dan akurasi validasi juga cukup tinggi meskipun fluktuatif, yang mengindikasikan potensi 
overfitting. Hal serupa terlihat pada grafik loss, di mana train_loss terus menurun, tetapi val_loss cenderung fluktuatif pada beberapa epoch.<br />
## Testing :dart:
![Demo GIF](https://github.com/sizubad/Face-Recognition/blob/736002e6cfb91ce8161e95e845c53c16c5d2a2b8/output_video_colab1.gif)<br/>
![Demo GIF](https://github.com/sizubad/Face-Recognition/blob/736002e6cfb91ce8161e95e845c53c16c5d2a2b8/output_video_colab.gif)<br/>
Secara keseluruhan, hasil prediksi model sudah menunjukkan kinerja yang baik, dengan akurasi keseluruhan mencapai 87%. Meskipun demikian, masih terdapat beberapa kesalahan 
dalam prediksi,yang terlihat dari variasi performa antar kelas
# Analisa Model :book:
Model yang kami gunakan **MobileNetV2** termasuk dalam kategori **deep learning** karena menggunakan arsitektur jaringan saraf dalam (deep neural network) yang terdiri dari 
banyak lapisan untuk memproses data. Berbeda dengan shallow learning, yang biasanya hanya melibatkan satu atau beberapa lapisan sederhana dalam model, MobileNetV2 dirancang 
untuk menangani data yang lebih kompleks dengan cara yang lebih efisien.
# Referensi :mag_right:
1. [Link Youtube :point_left:](https://www.youtube.com/watch?v=Ax6P93r32KU)
