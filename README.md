# Toturial menjalankan aplikasi fabcar dengan hyperledger fabric

1. Jalankan docker (tutorial disini menggunakan windows, menggunakan docker desktop)<br>
2. Cloning repository github (link menyusul di deskripsi)<br>
3. Jalankan linux shell (WSL2)<br>
4. Jalankan perintah ./install-fabric d<br>
   d : menjalankan daemon docker<br>
   <i>jika lihat di tutorial hyperfabric menggunakan perintah ./install-fabric d s (s : install sample)</i><br>
5. masuk ke folder network<br>
6. jalankan perintah ./network.sh down<br>
7. jalankan perintah ./network.sh up<br>
8. Saatnya jalankan smart contract aplikasi fabcar :<br>
   - masuk ke folder fabcar<br>
   - jalankan perintah ./startFabric.sh<br>
   - secara default smart contract fabcar menggunakan bahasa pemograman golang, jika ingin menggunakan<br>
     bahasa pemograman lain seperti javascript bisa menjalankan perintah ./startFabric.sh javascript<br>
   - daftarkan admin dengan perintah node enrollAdmin.js, tapi sebelumnya perlu install dahulu<br>
     dependency dengan perintah npm install (nasuk terlebih dahulu ke folder javascript lalu jalankan<br>
     perintah npm install)<br>
   - jalankan perintah node enrollAdmin.js dan node registerUser.js<br>
   - untuk melihat data initial yang ada di blockchain nya menggunakan perintah node query.js<br>
9. Menampilkan data blockchain menggunakan postman :<br>
   - jalankan aplikasi backend dengan perintah node backend.js<br>
   - untuk mendapatkan data jalankan url http://localhost:9003/api/queryallcars di postman<br>
   - untuk menambahkan data ke blockchain menggunakan method post dengan path url http://localhost:9003/api/addcar<br>
     dilengkapy payload pada body nya<br>

demikian tutorial aplikasi fabcar hyperledger fabric, tutoral berikut nya menampilkan data blockchain<br>
menggunakan hyperledger explorer.<br>
