# HeatMap Effective Reproductive Number COVID-19
Terimakasih kepada Bu Unan atas rekomendasi [paper ini](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3551767). Projek ini adalah respond saya atas minimnya informasi fundamental yang tersedia dan guna untuk memperkaya instrumen yang dapat digunakan sebagai pertimbangan atas transmisi wabahvirus nCOVID19. Goal dari proyek ini adalah penyajian visualisasi nilai Effective Reproductive Number (R) di pulau Jawa menggunakan metode perhitungan nilai R yang dipublikasikan dalam papers [High Temperature and High Humidity Reduce the Transmission of COVID-19](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3551767) yang diterbitkan oleh Social Science Research Network dengan parameter suhu dan kelembaban yang datanya diambil dari API Pengamatan Cuaca. Harap priksa kembali validasi dari data yang didapatkan, karena proyek ini masih pada tahap pengembangan.

## Visualisasi Data
### Versi 2 Visualisasi R number Pulau jawa
Menggunakan 768 data point yang didapatkan dengan memanggil [API openWeaterMap](https://openweathermap.org/current) dan menampilkan nilai R yang telah dikalkulasi ke dalam heatmap
<img src= https://github.com/wimbuhAdi/HeatMapCOVID-19-Effective-Reproductive-Number-DIY/blob/master/Node-red%20HeatMap%20Visualizer/heatMapJawa.jpg>

### Versi 1 visualisasi R number Ringroad
<img src= https://github.com/wimbuhAdi/HeatMapCOVID-19-Effective-Reproductive-Number-DIY/blob/master/Node-red%20HeatMap%20Visualizer/ringRoadheatMap.jpg width="320">   <img src= https://github.com/wimbuhAdi/HeatMapCOVID-19-Effective-Reproductive-Number-DIY/blob/master/Node-red%20HeatMap%20Visualizer/With%20Background%20Ring%20Road%20heatMap.jpg width="320">

### Flow realtime Node-red
<img src=https://github.com/wimbuhAdi/HeatMapCOVID-19-Effective-Reproductive-Number-DIY/blob/master/Node-red%20HeatMap%20Visualizer/flow_heatmap.jpg width="720">

## Setup dan Dependensi
### Setup
* Install Node-red : ikuti langkah-langkah di [laman resmi Node-Red](https://nodered.org/docs/getting-started/windows)
  * install [node UI HeatMap](https://flows.nodered.org/node/node-red-contrib-ui-heatmap)
* Data Ingest dan Interkoneksi Program : insatll linrary request di python (diuji di python 3) untuk get http API
```
pip install requests
```
  * lalu daftar [akun OpenWeaterAPI](https://openweathermap.org/) untuk mendapat token guna mengakses data cuaca
* install Paho MQTT library :
Ikuti langkah instalasi [ini](https://mosquitto.org/blog/2013/12/paho-mqtt-python-client/)
* Dapat digunakan cloud broker atau [local broker](http://www.steves-internet-guide.com/install-mosquitto-broker/)
### Dependnsi
* Local directori berisi file PNG untuk penyimpanan gambar peta background di node-red, di spesify di node  _file in_. 
<img src=https://github.com/wimbuhAdi/HeatMapCOVID-19-Effective-Reproductive-Number-DIY/blob/master/Node-red%20HeatMap%20Visualizer/dataPULL.jpg width="320">
