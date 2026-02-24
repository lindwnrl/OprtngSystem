<h1 align="center">Jobsheet 1 - Sistem Operasi</h1>

**Nama**        :Lindhu Nuril Rahmatdanto
**NIM**         :254107020216
**Kelas**       :TI 1G
**No Absen**    :17

## 1.10. Latihan

### 1.10.1 Latihan Konseptual

### 1. Jelaskan 5 fungsi utama sistem operasi dengan kongkret dari minimal 2 OS berbeda

#### Fungsi utama OS

##### 1.Process Management
    Fungsi : Mengatur pembuatan proses, eksekusi, penjadwalan CPU, multitasking, dan penghentian proses.
    
    Contoh di Windows 11 :
    1.Task Manager menampilkan proses aktif (Chrome, VS Code, dll).

    2.Windows menjadwalkan CPU agar beberapa aplikasi bisa berjalan bersamaan.

    3.Proses bisa dihentikan secara paksa lewat End Task.

    Contoh di Ubuntu
    1.Perintah ps, top, htop untuk melihat proses.

    2.kill PID untuk menghentikan proses.

    3.Kernel Linux mengatur penjadwalan CPU (CFS – Completely Fair Scheduler).    

##### 2.Memory Management
    Fungsi : Mengatur alokasi RAM, dealokasi, virtual memory, paging, dan mencegah konflik antar proses.

    Contoh di windows 11 :
    1. Task Manager menampilkan pemakaian RAM tiap aplikasi.

    2.Virtual Memory (pagefile.sys) digunakan saat RAM hampir penuh.

    3.Aplikasi berat (misalnya browser dengan banyak tab) tetap bisa berjalan meski RAM terbatas.

    Contoh di Ubuntu : 
    1.free -h untuk melihat penggunaan RAM.

    2.Swap digunakan saat RAM penuh.

    3.Kernel Linux mencegah satu program mengambil seluruh RAM.

##### 3. File Management
    Fungsi : Mengatur penyimpanan data: membuat, membaca, menulis, menghapus file/folder, serta struktur direktori.

    Contoh di Windows 11 : 
    1.File Explorer untuk membuat folder, copy–paste file.

    2.Sistem file NTFS mengatur izin dan struktur folder.

    3.Recycle Bin sebagai mekanisme penghapusan sementara.

    Contoh di Ubuntu : 
    1.File Manager (Nautilus) untuk operasi file grafis.

    2.Terminal: cp, mv, rm, mkdir.

    3.Sistem file seperti ext4 mengatur struktur dan hak akses file.

#####    4. Manajemen Perangkat Keras (Device Management)

    Fungsi:
    Mengatur komunikasi antara software dan hardware melalui driver (printer, keyboard, mouse, VGA, disk, dll).

    Contoh di Windows 11:

    1.Device Manager untuk melihat driver perangkat.

    2.Driver printer/VGA biasanya otomatis terinstal (Plug and Play).

    3.Jika driver rusak, perangkat bisa tidak berfungsi normal.

    Contoh di Ubuntu:

    1.Banyak driver sudah terintegrasi di kernel Linux.

    2.Perangkat USB langsung dikenali tanpa instal manual.

    3.Driver GPU tertentu (NVIDIA) perlu instalasi tambahan.

##### 5. Antarmuka Pengguna (User Interface)

    Fungsi:
    Menyediakan cara interaksi pengguna dengan komputer: GUI (grafis) dan CLI (command line).

    Contoh di Windows 11:

    1.GUI: Desktop, Start Menu, Taskbar.

    2.CLI: Command Prompt & PowerShell untuk perintah teks.

Contoh di Ubuntu:

    1.GUI: Desktop GNOME (ikon, menu aplikasi).

    2.CLI: Terminal (bash) untuk administrasi dan scripting.

### Kapan sebaiknya menggunakan Windows vs Linux vs macOS? Analisis berdasarkan use case: gaming, development, server, creative work, dan enterprise.

#### Analisis :

####   1. Gaming

Windows 11
Paling direkomendasikan untuk gaming.
Alasan:

    1.Kompatibilitas game tertinggi (hampir semua game PC native Windows).

    2.Dukungan driver GPU terbaik (NVIDIA/AMD).

    3.Anti-cheat (Easy Anti-Cheat, BattlEye) mayoritas stabil di Windows.

    Contoh konkret:

    Game AAA (Cyberpunk, Elden Ring, Valorant) berjalan native tanpa layer tambahan.

    Platform game PC utama memprioritaskan Windows.

Linux (kurang ideal untuk gaming kompetitif):
Ubuntu

    1.Banyak game bisa jalan via Proton/Wine, tapi tidak semua.

    2.Game dengan anti-cheat kernel-level sering tidak bisa jalan.
    Alternatif: Dual boot Windows + Linux.

macOS (tidak direkomendasikan untuk gaming):
macOS

    1.Koleksi game terbatas.

    2.Banyak game Windows tidak tersedia native di macOS.
    Alternatif: Gunakan Windows untuk gaming.


#### 2. Software Development / Programming

Linux (paling ideal untuk development backend, sistem, cloud):
Ubuntu
Alasan:

    1.Lingkungan mirip server production (Linux-based).

    2.Native support Docker, Kubernetes, toolchain C/C++, Python, Java, Node.js.

    3.Lebih stabil untuk workflow DevOps.

Windows (baik untuk fullstack & game dev):
Windows 11
Alasan:

    1.Visual Studio sangat kuat untuk .NET & game dev (Unity).

    2.WSL (Windows Subsystem for Linux) membuat Linux environment bisa dipakai di Windows.

    3.Cocok untuk dev yang butuh software Windows-only.

macOS (ideal untuk mobile dev Apple & UI dev):
macOS
Alasan:

    1.Wajib untuk iOS/macOS development (Xcode).

    2.Terminal Unix-like → nyaman untuk web/backend.

    3.Performa stabil untuk developer kreatif.


#### 3. Server (Web Server, Cloud, Database, Backend)

Linux (standar industri server):
Ubuntu Server
Alasan:

    1.Ringan, stabil, hemat resource.

    2.Mayoritas server dunia pakai Linux.

    3.Gratis, aman, update cepat.

Windows Server (dipakai jika ekosistem Microsoft):
Windows Server 2022
Alasan:

    1.Cocok untuk Active Directory, .NET enterprise, SQL Server.

    2.Integrasi kuat dengan infrastruktur Microsoft.

macOS (tidak layak untuk server):

    1.macOS bukan OS server produksi.

    2.Tidak dipakai di data center profesional.
    Alternatif: Linux atau Windows Server.

#### 4. Creative Work (Desain, Video Editing, Musik, 3D)

macOS (unggul untuk kreator profesional):
macOS
Alasan:

    1.Ekosistem kreatif kuat (Final Cut, Logic Pro).

    2.Stabilitas tinggi untuk editing video/audio.

    3.Integrasi hardware–software optimal.

Windows (fleksibel & kuat untuk 3D/VFX):
Windows 11
Alasan:

    1.Software kreatif populer (Adobe, Blender) full support.

    2.Dukungan GPU NVIDIA CUDA untuk render 3D & AI.

    3.Lebih bebas upgrade hardware.

Linux (kurang cocok untuk creative mainstream):
Ubuntu

    1.Banyak software open-source (GIMP, Krita, Blender).

    2.Tidak cocok jika workflow butuh Adobe / plugin industri tertentu.
    Alternatif: Windows/macOS.


#### 5. Enterprise / Perkantoran / Corporate IT

Windows (standar enterprise desktop):
Windows 11
Alasan:

    1.Kompatibel dengan software kantor (Office, ERP, accounting).

    2.Integrasi Active Directory.

    3.Support vendor luas.

Linux (untuk server & workstation teknis):
Ubuntu

    1.Digunakan di server enterprise, cloud, data center.

    2.Workstation engineer (IT, data scientist, sysadmin).

macOS (enterprise kreatif & eksekutif):
macOS

    1.Umum di perusahaan kreatif & startup teknologi.

    2.Kurang umum di enterprise tradisional (akuntansi/manufaktur).

### Intalasi Ubuntu

#### 1. Download Ubuntu Server ISO dari website resmi 
#### 2. Create VM baru di VirtualBox (RAM: 2GB, Disk: 25GB)
#### 3. Install dengan automatic partitioning (guided)
#### 4. Buat user account dengan password yang kuat
(Mohon maaf bapak tapi saya menggunakan Windows Support System for Linux,)
#### 5. Reboot dan login ke sistem
![alt text](image.png)
#### 6. Dokumentasikan proses instalasi dengan screenshot key steps

### Pasca Instalasi Ubuntu
1. Update package list
![alt text](image-1.png)
2. Upgrade packages
![alt text](image-2.png)
3. Install neofetch
![alt text](image.png)
4. Run neofetch
![alt text](image-1.png)
5. Disk Usage
![alt text](image-2.png)
6. Check Memory
![alt text](image-3.png)

### Eksplorasi sistem
1. Tampilkan Info
![alt text](image-4.png)
2. Tampilkan Versi Kernel
![alt text](image-5.png)
3. List Partisi
![alt text](image-6.png)
4. Check network connectivity
![alt text](image-7.png)
5. htop
![alt text](image-8.png)
6. Laporan singkat
Sistem Operasi :Ubuntu 24.04.4 LTS on Windows 10 x86_64 telah berhasil di install
kernel :6.6.87.2-microsoft-standard-WSL2
Network : 4 packets transmitted, 4 received, 0% packet loss, time 3005ms
rtt min/avg/max/mdev = 37.923/140.587/249.914/99.702 ms

### Latihan Refleksi 
 1. Sistem operasi apa yang Anda        gunakan sehari-hari? (Windows, macOS,
 Linux, atau lainnya)

    Sebelumnya saya menggunakan window sebagai sistem operasi di laptop saya dan belum pernah menggunakan sistem operasi lain

 2. Berapa lama Anda menggunakan sistem operasi tersebut?

    Kurang lebih 4 tahun saya menggunakan sistem operasi ini

 3. Apa yang Anda sukai dari sistem operasi tersebut?

    Sistem Operasi window sangat user friendly dibuktikan dengan banyaknya user yang mudah paham menggunakan sistem operasi ini

 4.  Apa tantangan atau masalah yang pernah Anda hadapi?

    Sejauh ini saya baik baik saja menggunakan window

 5. Apakah Anda pernah menggunakan sistem operasi lain? Bandingkan
pengalaman Anda.

    Sebelumnya saya belum pernah memakai sistem operasi lain selain window

6. Setelah mempelajari bab ini, apakah ada sistem operasi lain yang ingin
Anda coba? Mengapa?

    Saya tertarik pada Sistem Operasi Linux dan mungkin kedepannya saya akan belajar linux untuk mengetahui lebih dalam tentangnya.Saya juga tertarik pada bidang ilmu CyberSecurity yang membutuhkan pemahaman mendalam tentang linux,untuk itulah saya tertarik untuk belajar linux dan menjadi Ethical Hacker

