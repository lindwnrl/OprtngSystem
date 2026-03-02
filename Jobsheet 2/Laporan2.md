<h1 align="center">Jobsheet 2 -Sistem Operasi</h1>


**Nama**        : Lindhu Nuril Rahmatdanto
**NIM**         : 254107020216
**Kelas**       : TI 1G
**No Absen**    : 17

## Praktikum 2

### 1. Tampilkan Inforamsi CPU
Informasi CPU (![alt text](image.png))

### 2. Tampilkan ringkasan memori
Informasi ringkasan memori (![alt text](image-1.png))
1. Jumlah CPU, Core/Thread : CPU fisik : 1, Core fisik : 4, Thread : 8
2. Total Ram : 8
3. Total Swap : 1.0Gi
4. Perbedaan RAM dan swap : RAM adalah memori utama yang dipakai CPU untuk menyimpan data & program yang masih run sedangkan swap adalah ruang di ssd/hdd yang dipakai OS sebagai cadangan apabila RAM penuh

### Latihan 2 
1. Temukan 1 perangkat PCI (misal NIC) dan tuliskan: Vendor:Device ID (angka
heksadesimal), nama driver/modul kernel, dan deskripsi singkat fungsinya.

Driver/Modul Kernel : dxgkrnl (
3d controler : microsoft corporation basic rende driver
)
Fungsi :
1. dxgkrnl adalah driver kernel Linux untuk WSL2 yang menjembatani akses GPU Windows ke Linux.

2. Digunakan untuk render grafis, akselerasi GPU, CUDA/DirectML di Linux yang berjalan di atas Windows.

3. Bukan driver GPU asli (bukan NVIDIA/Intel langsung), melainkan lapisan translasi dari Windows ke Linux.

Driver/Modul Kernel: virtio-pci (SCSI storage controller: Red Hat, Inc. Virtio 1.0 console)
Fungsi :
1. virtio-pci adalah driver virtual   device untuk VM (KVM/QEMU/Hyper-V).

2. Menghubungkan Linux guest dengan hardware virtual milik host.

Driver /Modul Kernel : virtio-pci(System peripheral: Red Hat, Inc. Virtio file system)
Fungsi : 
1. Digunakan untuk sharing filesystem antara host (Windows) dan Linux guest.

2. Di WSL2, ini dipakai untuk mount drive Windows (/mnt/c, dll).

3. Memungkinkan Linux membaca/menulis file di Windows host.

### Latihan 2.3

Dari output ls -l, jelaskan perbedaan penanda file untuk block device dan
character device. (Hint: karakter pertama pada permission string)

Perbedaan ls -l /dev/sda dan ls -l /dev/tty ada pada jenis perangkat yang direpresentasikan di Linux. Keduanya adalah device file, tapi fungsinya sangat berbeda: satu untuk storage block device, satu untuk terminal karakter device.

Makna:

1. /dev/sda = perangkat disk pertama (HDD/SSD).

2. Biasanya berisi partisi seperti /dev/sda1, /dev/sda2, dst.

------------------------------------------

3. /dev/tty = terminal (TTY) yang sedang kamu pakai saat ini.

4. Bukan file di disk, tapi antarmuka input/output.

### Latihan 2.4
Gunakan grep untuk menampilkan hanya baris yang mengandung INFO atau
WARN dari data.log. (Hint: gunakan grep -E dengan pola alternatif)

![alt text](<../Jobsheet 1/foto copy/grep -E.png>)
Saya menggunakan grep -E untuk menampilkan hanya satu baris informasi yang saya program

### Latihan 2.A
Jalankan lspci -nnk. Pilih 1 perangkat PCI dan tuliskan: nama perangkat,
ID vendor:device, dan kernel driver in use.

![alt text](image.png)
nama perangkat : SCSI storage controller 
Vendor : Red Hat,Inc Virtio 1.0 console
Vendor ID : 1af4
Kernel  : virtio-pci

### Latihan 2.B
Tentukan device root filesystem dengan findmnt /. Lalu cocokkan dengan
lsblk -f dan tuliskan tipe filesystem serta UUID-nya.


### Latihan 2.C
Buat file server.log berisi minimal 10 baris dengan variasi kata: INFO,
WARN, ERROR. Gunakan grep untuk menampilkan hanya baris ERROR.
### Latihan 2.D
Gunakan sed untuk mengganti semua kata server menjadi node pada file
latihan. Tunjukkan sebelum dan sesudah.
### Latihan 2.E
Gunakan df -h lalu awk untuk menampilkan filesystem yang penggunaan disk
di atas 70%.
### Latihan 2.F
Jalankan sleep 600 &. Temukan PID-nya dengan ps. Hentikan dengan
SIGTERM. Jelaskan beda SIGTERM vs SIGKILL.
### Latihan 2.G
Gunakan systemctl –failed. Jika tidak ada yang gagal, pilih satu service
aktif (misal ssh) dan tampilkan status serta 30 baris log terakhirnya.
