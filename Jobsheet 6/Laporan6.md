<h1 align = "center">Jobsheet 6 - Sistem Operasi </h1>

```
Nama        :Lindhu Nuril Rahmatdanto
NIM         :254107020216
Kelas       :TI 1G  
No Absen    :17
```

## Latihan 6.1
Jalankan ps aux dan amati outputnya:

1. Berapa total proses yang berjalan? Proses apa yang memiliki PID terkecil?
Terdapat 20 proses yang berjalan setelah command ps -aux dijalankan dan proses dengan PID terkecil ada pada proses root pertama dengan PID 1

2. Jalankan pstree -p dan temukan proses bash Anda. Proses apa yang menjadi induk (PPID) dari bash tersebut?
Proses yang menjadi Parent PID dari bash tersebut adalah 384

3. Bandingkan output ps aux dan ps aux -L. Apa perbedaan yang Anda lihat?
Perbedaan antara ps aux dan ps aux -L adalah ps aux hanya menampilkan proses sedangkan ps aux -L menampilkan proses dan thread di dalamnya sehingga ps aux -L lebih lengkap

## Latihan 6.2
1. Jalankan sleep 120 & dan amati kolom STAT pada ps aux. Kondisi apa yang ditampilkan? Mengapa proses sleep berada di kondisi tersebut?
Setelah menjalankan proses ps aux akan terlihat di bagian bawah bahwa proses sleep sebelumnya berstatus S dan dalam kondisi idle 

2. Jalankan beberapa perintah yang berhasil dan yang gagal, lalu catat exit code masing-masing. Pola apa yang Anda temukan?
Pola yang saya temukan adalah bahwa apabila proses berhasil dijalankan exit code yang keluar adalah 0 sedangkan kalau gagal angkanya adalah selain 0.

## Latihan 6.3
1. Jalankan nice -n 5 sleep 200 & dan verifikasi nilai NI-nya dengan ps.

2. Ubah nilai nice menjadi 10 menggunakan renice, lalu verifikasi kembali.

3. Coba ubah nilai nice menjadi -5 tanpa sudo. Apa yang terjadi? Mengapa Linux membatasi hal ini untuk user biasa?
Karena adanya permission yang menghalangi user untuk mengubah nice value menjadi -5,user hanya boleh menaikkan nice value dari 0 - 10

## Latihan 6.4
1. Jalankan sleep 400 &, kirim SIGSTOP, dan amati perubahan  kolom STAT. Kondisi apa yang muncul?
Setelah menjalankan instruksi yang ada kolom stats pada PID sleep 400 berubah menjadi T (Stopped)
2. Kirim SIGCONT dan verifikasi proses kembali berjalan.
Setelah menjalankan proses SIGCONT kolom stats yang awalnya T menjadi S.
3. Hentikan proses dengan SIGTERM lalu verifikasi sudah tidak ada. Kapan Anda memilih SIGKILL daripada SIGTERM?
SIGKILL dipilih apabila SIGTERM tidak bisa mematikan program secara aman karena pada dasarnya SIGKILL berfungsi untuk mematikan program secara paksa

## Latihan 6.5
1. Jalankan top di foreground. Apa yang terjadi di terminal?
Terminal akan dipenuhi oleh program yang menampilkan kondisi real-time dan selama program top masih berjalan user tidak bisa menjalankan program lain
2. Tekan Ctrl+Z dan cek statusnya dengan jobs. Kondisi apa yang ditampilkan?
Program top akan menampilkan status stopped
3. Pindahkan ke background dengan bg. Apakah top dapat berjalan dengan baik di background? Mengapa?
Program top bisa dijalnkan di background hanya saja tidak menampilkan apa apa di terminal
4. Kembalikan ke foreground dengan fg, lalu keluar dengan q .

## Latihan 6.6
1. Gunakan ps aux –sort=%mem untuk menemukan proses yang menggunakan memori paling banyak di VM Anda. Proses apa itu?
Proses yang memakan memori paling banyak adalah proses root
2. Di dalam top, tekan 1 . Apa yang berubah pada tampilan? Mengapa informasi ini berguna?
Informasi ini berguna karena user bisa melihat kinerja semua core CPU
3. Di dalam htop, navigasikan ke proses sshd menggunakan tombol panah. Tekan F9 dan amati opsi sinyal yang tersedia.
Terdapat 16 opsi yang tersedia di dalam pilihannya.

## Latihan 6.A
1. Jalankan ps aux –forest dan temukan proses dengan PID 1. Apa nama dan fungsi proses tersebut dalam sistem Linux modern?
Proses root ini berfungsi untuk memproses pertama saat boot dan adalah induk semua proses
2. Hitung berapa proses yang dimiliki oleh user root dan berapa yang dimiliki oleh user Anda. Mengapa root memiliki lebih banyak proses?
Terdapat 14 proses root dan 5 proses dari user.Hal ini karena root mengatur system sehingga butuh proses lebih intens daripada user itu sendiri
3. Temukan semua proses yang berada dalam kondisi S. Mengapa sebagian besar proses di sistem berada dalam kondisi ini?
Proses itu adlah interruptible sleep yang artinya walaupun dalam keadaan sleep proses itu masih bisa diaktifkan kembali.Ini karena sebagian proses bersifat menunggu diaktifkan daripada aktif terus.

## Latihan 6.B
1. Jalankan tiga perintah sleep dengan durasi 100, 200, dan 300 detik di background. Verifikasi ketiganya dengan jobs.

2. Bawa job kedua ke foreground, jeda dengan Ctrl+Z , lalu kembalikan ke background dengan bg.

3. Hentikan job pertama dengan kill %1. Tampilkan kembali daftar job. Berapa job yang tersisa?
Ada 2 jobs tersisa yang msih berjalan di belakang layar sedangkan 1 lainnya dengan status terminated

## Latihan 6.C
1. Jalankan dua proses sleep: satu dengan nice +5 dan satu dengan nice +15. Verifikasi nilai NI keduanya dengan ps.

2. Gunakan renice untuk mengubah nice proses pertama menjadi +10.Proses mana yang kini lebih diprioritaskan scheduler?
Tidak ada yang diprioritaskan karena Scheduler Linux akan membagi CPU secara adil dan kedua proses ini mendapat jatah waktu yang sama
3. Kirim SIGSTOP ke salah satu proses, verifikasi kondisi T-nya, lalu kirim SIGCONT. Akhiri semua proses percobaan dengan pkill sleep




