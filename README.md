# Jarkom-Modul-4-T1-2021

## Anggota Kelompok

- Prima Secondary Ramadhan  05311940000001
- Asiyah Hanifah            05311940000002
- Widya Inayatul            05311940000010
---

## 1. VLSM 

## Topologi VLSM Pada CPT
Pertama adalah membuat topologi VLSM menggunakan Cisco Packet Tracer seperti yang diminta pada soal shift
![topologi vlsm](https://user-images.githubusercontent.com/73151978/143517757-4fce7c41-3957-4859-9b3c-33e66f657af6.png)

## Hasil Perhitungan VLSM

Hasil perhitungan Jumlah IP, dan Netmask dari Subnet yang sudah dibuat.
Contoh perhitungan: pada subnet A1 terdapat jumlah IPnya yaitu 721. Karena jumlah IPnya 721 maka subnet A1 merupakan netmask /22 karena jumlah IP A1 kurang dari IP netmask /22 yaitu 1024. Artinya A1 termasuk dalam area netmask /22. Dari perhitungan ini didapat Jumlah IP dan Netmask semua subnet yang ada pada tabel sebagai berikut.

![LABELLING](https://user-images.githubusercontent.com/73151978/143518172-9a96aa33-95ca-4f99-b739-5fa30f201215.png)

## Subnetting
menghitung pembagian IP berdasarkan NID dan netmask menggunakan pohon seperti gambar di bawah. Kemudian dilakukan subnetting dengan menggunakan pohon untuk pembagian IP sesuai dengan kebutuhan masing-masing subnet yang ada.

![pohon](https://user-images.githubusercontent.com/73151978/143518484-98c20bbb-6bef-4fec-b58e-eb89aba094af.jpg) 

melakukan subnetting pohon untuk pembagian IP dengan bantuan tabel subnet tersebut

![tabel ajaib](https://user-images.githubusercontent.com/73151978/143518674-39973491-0bd6-4fe3-906e-d4599193ad7a.png)

## Hasil perhitungan Network ID, Netmask, Broadcast Address
Dari pohon tersebut akan mendapat pembagian IP dengan melakukan perhitungan.
Hasil perhitungan Network ID, Netmask, Broadcast Address dari subnet yang telah ditentukan netmasknya.
Contoh perhitungan: pada subnet A1 yang memiliki Network ID yaitu 10.42.20.0 dengan Netmasknya 255.255.252.0 yang didapatkan berdasarkan pohonnya sesuai tabel di atas. Kemudian untuk menentukan broadcast address kami lakukan perhitungan sebagai berikut.
```
IP			    : 10.42.20.0
Bit			    : 00001010.00101010.000101 00.00000000
Netmask		    : 255.255.252.0
Bit			    : 11111111.11111111.111111 00.00000000
Invert Netmask	: 00000000.00000000.000000 11.11111111
Kemudian melakukan operasi OR pada IP dan Invert Netmasknya.
IP			    : 00001010.00101010.000101 00.00000000
Netmask		    : 00000000.00000000.000000 11.11111111
------------------------------------------------------------------------------------------------ Operasi OR
Bit Broadcast	: 00001010.00101010.000101 11.11111111
Broadcast		: 10.42.23.255
```

Sehingga didapatkan Broadcast Address dari subnet A1 dengan NID 10.42.20.0 adalah 10.42.23.255. Dari perhitungan tersebut, kami dapatkan hasil perhitungan Network ID, Netmask, Broadcast Address dari semua subnet pada tabel berikut.

![tabel perhitungan IP](https://user-images.githubusercontent.com/73151978/143518929-1bf891a3-3618-4e0a-a1e0-b650fe2816b4.png)

## Konfigurasi Pembagian IP dan Subnet Pada CPT
Setelah melakukan pembagian IP, kami memasukkan hasil pembagian IP dan subnetnya ke dalam CPT. Sebagai contoh pada subnet A1 yang memiliki NID 10.42.20.0. Maka pada router Seastone yang mengarah ke Elena pada lingkup A1 tepatnya di Fa 0/1 nya diberi IP Configuration 10.42.20.1. Sedangkan pada Elena IP addressnya diisi 10.42.20.2 dan IP Gatewaynya diisi IP dari Seastone yaitu 10.42.20.1. Seperti gambar berikut.

![s0](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/s0.png)

![e1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/e1.png)

## Routing
Untuk routing kita harus mendaftarkan atau menambahkan route yang tidak dikenali oleh router tersebut, karena tidak berdekatan.
### Foosha
![f1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/f1.png)

![f2](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/f2.png)


![f3](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/f3.png)

![f4](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/f4.png)

### Water 7
![w1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/w1.png)

### Pucci
![p1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/p1.png)

### Guanhao
![g1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/g1.png)

### Oiimo
![o1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/o1.png)

### Seastone
![s1](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/s1.png)

## 2. CIDR

## Topologi CIDR Pada GNS3
Selanjutnya kami membuat topologi CIDR menggunakan GNS3 seperti yang diminta pada soal shift

![GNS3](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/gns3.png)

## Perhitungan teknik CIDR 

- Class A, B, dan C

Pertama menggabungkan hingga menjadi class A seperti A1, A2, dst.  Subnet B1 merupakan hasil penggabungan dari subnet A1 dengan A2. B1 memiliki netmask / 21 karena A1= /22 dan A2=/24 Lalu ulangi langkah tersebut. Subnet C1 merupakan hasil penggabungan dari subnet B1 dengan B2 seperti gambar berikut.

![VLSM B C](https://user-images.githubusercontent.com/73151978/143519254-15e3d097-5ad4-4a78-821f-ea29022c22c2.png)

- Class D dan E

Subnet D1 merupakan hasil penggabungan dari subnet C1 dengan D2. Subnet E1 merupakan subnet besar yang mencakup 1 topologi dari proses penggabungan didapatkan subnetnet besar /17 dengan NID 10.42.0.0, netmask 255.255.128.0. Seperti gambar berikut.

![VLSM D   E](https://user-images.githubusercontent.com/73151978/143519258-f927abe7-3c18-4cc2-9687-ed2969d6053d.png)

## Subnetting
Kemudian kami menentukan pembagian IP berdasarkan NID dan netmask menggunakan pohon seperti gambar di bawah. Kemudian dilakukan subnetting dengan menggunakan pohon untuk pembagian IP sesuai dengan kebutuhan masing-masing subnet yang ada.

![tree fix](https://user-images.githubusercontent.com/73151978/143673918-58e928be-0e1e-475d-b923-f17e61dbd3c1.png)

Dalam menentukan pembagian IP pada subnetting pohon CIDR ini, kami melakukan pencocokan dengan bantuan tabel berikut.

![tabel ajaib](https://user-images.githubusercontent.com/73151978/143518674-39973491-0bd6-4fe3-906e-d4599193ad7a.png)


## Hasil perhitungan Network ID, Netmask, Broadcast Address
Berdasarkan pohon CIDR yang telah dibuat kami mendapatkan pembagian IP dengan melakukan perhitungan. Hasil perhitungan Network ID, Netmask, Broadcast Address dari subnet yang telah ditentukan netmasknya.

Contoh perhitungan: pada subnet A1 yang memiliki Network ID yaitu 10.42.0.0 dengan Netmasknya 255.255.252.0 yang didapatkan berdasarkan pohonnya sesuai tabel di atas. Kemudian untuk menentukan broadcast address kami lakukan perhitungan sebagai berikut.

```
IP			    : 10.42.0.0
Bit			    : 00001010.00101010.000000 00.00000000
Netmask		    : 255.255.252.0
Bit			    : 11111111.11111111.111111 00.00000000
Invert Netmask	: 00000000.00000000.000000 11.11111111

Kemudian melakukan operasi OR pada IP dan Invert Netmasknya.
IP			    : 00001010.00101010.000000 00.00000000
Netmask		    : 00000000.00000000.000000 11.11111111
------------------------------------------------------------------------------------------------ Operasi OR
Bit Broadcast	: 00001010.00101010.000000 11.11111111
Broadcast		: 10.42.3.255
```

Sehingga didapatkan Broadcast Address dari subnet A1 dengan NID 10.42.20.0 adalah 10.42.23.255. Dari perhitungan tersebut, kami dapatkan hasil perhitungan Network ID, Netmask, Broadcast Address dari semua subnet pada tabel berikut.

![fix tabel cidr](https://user-images.githubusercontent.com/73151978/143673772-a6355bc0-ff67-43a1-a77c-84519b5638db.png)

## Konfigurasi Pembagian IP dan Subnet Pada GNS3
Setelah melakukan pembagian IP, kami memasukkan hasil pembagian IP dan subnetnya ke dalam GNS3 untuk caranya cukup mirip dengan pengimplementasian konfigurasi pada CPT. Bedanya pada GNS3 diberi pada eth 0, eth1, eth2, dan lain-lain sesuai dengan subnet. Tidak lupa juga diberi gateway untuk alur jalannya. Berikut ini contoh konfigurasi pada GNS3 di Foosha dan Water 7 untuk subnet A8.

1. Foosha
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.42.64.1
	netmask 255.255.252.0
	broadcast 10.42.67.255

auto eth2
iface eth2 inet static
	address 10.42.72.1
	netmask 255.255.255.252
	broadcast 10.42.72.3


auto eth3
iface eth3 inet static
	address 10.42.68.1
	netmask 255.255.255.252
	broadcast 10.42.68.3

auto eth4
iface eth4 inet static
	address 10.42.20.1
	netmask 255.255.255.252
	broadcast 10.42.20.3
```
2. Water 7
```
auto eth0
iface eth0 inet static
	address 10.42.68.2
	netmask 255.255.255.252
	broadcast 10.42.68.3
        gateway 10.42.68.1

auto eth1
iface eth1 inet static
	address 10.42.48.1
	netmask 255.255.252.0
	broadcast 10.42.67.255
        gateway 10.42.68.1

auto eth2
iface eth2 inet static
	address 10.42.52.1
	netmask 255.255.255.252
	broadcast 10.42.52.3
        gateway 10.42.68.1

```
## Routing
Untuk routing kita harus mendaftarkan atau menambahkan route yang tidak dikenali oleh router tersebut, karena tidak berdekatan pada GNS3.

1. Foosha
```
# masquerade dengan netmask terbesar /17
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 10.42.0.0/17

# ke a11 JIPANGU
route add -net 10.42.40.0 netmask 255.255.255.128 gw 10.42.68.2

# ke a13 client BLUENO
route add -net 10.42.64.0 netmask 255.255.252.0 gw 10.42.64.2

# ke a12 client CIPHER
route add -net 10.42.48.0 netmask 255.255.252.0 gw 10.42.68.2

# ke a9 PUCCI
route add -net 10.42.52.0 netmask 255.255.255.252 gw 10.42.68.2

# ke a10 CALMBELT dan COURT YARD
route add -net 10.42.32.0 netmask 255.255.248.0 gw 10.42.68.2

# ke a8 WATER7
route add -net 10.42.68.0 netmask 255.255.255.252 gw 10.42.68.2

# ke a5 JORGE
route add -net 10.42.26.0 netmask 255.255.255.240 gw 10.42.20.2

# ke a3 OIIMO
route add -net 10.42.8.0 netmask 255.255.255.252 gw 10.42.20.2

#ke a6 JABRA
route add -net 10.42.16.0 netmask 255.255.252.0 gw 10.42.20.2

#ke DORIKI
route add -net 10.42.72.0 netmask 255.255.255.252 gw 10.42.72.2

#ke GUANHAO
route add -net 10.42.20.0 netmask 255.255.255.252 gw 10.42.20.2

# ke a4 MAINGATE
route add -net 10.42.24.0 netmask 255.255.254.0 gw 10.42.20.2

# ke a15 FUKUROU
route add -net 10.42.8.4 netmask 255.255.255.252 gw 10.42.20.2

# ke a2 ENIESLOBBY
route add -net 10.42.4.0 netmask 255.255.255.0 gw 10.42.20.2

# a1 ELENA
route add -net 10.42.0.0 netmask 255.255.252.0 gw 10.42.20.2

```
b. Water7
```
#ke a11 JIPANGU
route add -net 10.42.40.0 netmask 255.255.255.128 gw 10.42.52.2

#ke a10 CALMBELT dan COURT YARD
route add -net 10.42.32.0 netmask 255.255.248.0 gw 10.42.52.2
```
c. Guanhao
```
# ke a15 FUKUROU
route add -net 10.42.8.4 netmask 255.255.255.252 gw 10.42.8.2

# ke a5 JORGE
route add -net 10.42.26.0 netmask 255.255.254.0 gw 10.42.24.2

# ke a1 ELENA
route add -net 10.42.0.0 netmask 255.255.252.0 gw 10.42.8.2

# ke a2 ENIESLOBBY
route add -net 10.42.4.0 netmask 255.255.255.0 gw 10.42.8.2
```
d. ke a1 Elena
```
ke a1 ELENA
route add -net 10.42.0.0 netmask 255.255.252.0 gw 10.42.4.2
```

## Testing Routing
1. Jabra ke Jipangu
![jj](https://raw.githubusercontent.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/main/images/jj.png)

2. Jabra ke Google
![jg](https://github.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/blob/main/images/jg.png?raw=true)

3. Elena ke Pucci dan Elena ke Google
![epg](https://github.com/asiyahhanifah/Jarkom-Modul-4-T1-2021/blob/main/images/epg.png?raw=true)
## Kendala
awalnya banyak tapi setelah saya memahami oh ternyata bisa.











